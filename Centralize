#Function to Centralize Write-Host Output, Just take string variable parameter and pads it
#Nerd Level over 9000!!! Ad-hoc Polymorphic power time!!
$pswwidth = (get-host).UI.RawUI.MaxWindowSize.Width
function Centralize()
{
  param(
  [Parameter(Position=0,Mandatory=$true)]
  [string]$S,
  [Parameter(Position=1,Mandatory=$false,ParameterSetName="color")]
  [string]$C
  )
    $sLength = $S.Length
    $padamt =  "{0:N0}" -f (($pswwidth-$sLength)/2)
    $PadNum = $padamt/1 + $sLength #the divide by one is a quick dirty trick to covert string to int
    $CS = $S.PadLeft($PadNum," ").PadRight($PadNum," ") #Pad that shit
    if ($C) #if variable for color exists run below
    {    
        Write-Host $CS -ForegroundColor $C #write that shit to host with color
    }
    else #need this to prevent output twice if color is provided
    {
        $CS #write that shit without color
    }
}
