---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 01f9d007d54e7e96ac28e81b5081dc696d3af406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591051"
---
# <span data-ttu-id="294d1-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="294d1-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="294d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="294d1-102">SYNOPSIS</span></span>
<span data-ttu-id="294d1-103">Sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="294d1-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="294d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="294d1-104">SYNTAX</span></span>

### <span data-ttu-id="294d1-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="294d1-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [<CommonParameters>]
```

### <span data-ttu-id="294d1-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="294d1-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [<CommonParameters>]
```

### <span data-ttu-id="294d1-107">UX</span><span class="sxs-lookup"><span data-stu-id="294d1-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication] [<CommonParameters>]
```

## <span data-ttu-id="294d1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="294d1-108">DESCRIPTION</span></span>
<span data-ttu-id="294d1-109">**Set-AzureRmVMOperatingSystem** cmdlet 'i sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="294d1-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="294d1-110">Oturum açma kimlik bilgilerini, bilgisayar adını ve işletim sistemi türünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="294d1-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="294d1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="294d1-111">EXAMPLES</span></span>

### <span data-ttu-id="294d1-112">Örnek 1: yeni sanal makinelerin işletim sistemi özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="294d1-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="294d1-113">İlk komut, parolayı güvenli bir dizeye dönüştürür ve $SecurePassword değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="294d1-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="294d1-114">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="294d1-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="294d1-115">İkinci komut, Kullanıcı Tamcağı ve $SecurePassword depolanan parola için bir kimlik bilgisi oluşturur ve $Credential değişkeninde kimlik bilgisini depolar.</span><span class="sxs-lookup"><span data-stu-id="294d1-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="294d1-116">Daha fazla bilgi için yazın `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="294d1-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="294d1-117">Üçüncü komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="294d1-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="294d1-118">Dördüncü komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="294d1-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="294d1-119">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="294d1-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="294d1-120">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="294d1-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="294d1-121">Sonraki dört komut, aşağıdaki komutta kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="294d1-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="294d1-122">Bu dizeleri doğrudan **set-AzureRmVMOperatingSystem** komutunda belirtebileceğinden, bu yaklaşım yalnızca okunabilirlik için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="294d1-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="294d1-123">Ancak, komut dosyalarında bu gibi bir yaklaşım kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="294d1-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="294d1-124">Son komut $VirtualMachine depolanan sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="294d1-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="294d1-125">Komut $Credential uygulamasında depolanan kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="294d1-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="294d1-126">Komut bazı parametrelerde önceki komutlarda atanan değişkenleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="294d1-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="294d1-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="294d1-127">PARAMETERS</span></span>

### <span data-ttu-id="294d1-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="294d1-128">-ComputerName</span></span>
<span data-ttu-id="294d1-129">Bilgisayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="294d1-130">-Credential</span></span>
<span data-ttu-id="294d1-131">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="294d1-132">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="294d1-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="294d1-133">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="294d1-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="294d1-134">-CustomData</span></span>
<span data-ttu-id="294d1-135">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="294d1-136">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="294d1-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="294d1-137">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="294d1-137">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="294d1-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="294d1-139">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="294d1-139">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-140">-Enableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="294d1-140">-EnableAutoUpdate</span></span>
<span data-ttu-id="294d1-141">Bu cmdlet 'in otomatik güncelleştirmeyi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="294d1-141">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-142">-Linux</span><span class="sxs-lookup"><span data-stu-id="294d1-142">-Linux</span></span>
<span data-ttu-id="294d1-143">İşletim sistemi türünün Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="294d1-143">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-144">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="294d1-144">-ProvisionVMAgent</span></span>
<span data-ttu-id="294d1-145">Ayarların sanal makinede sanal makine aracısının yüklü olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-145">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="294d1-146">-TimeZone</span></span>
<span data-ttu-id="294d1-147">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-147">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-148">-VM</span><span class="sxs-lookup"><span data-stu-id="294d1-148">-VM</span></span>
<span data-ttu-id="294d1-149">İşletim sistemi özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-149">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="294d1-150">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="294d1-150">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="294d1-151">New-AzureRmVMConfig cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="294d1-151">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-152">-Windows</span><span class="sxs-lookup"><span data-stu-id="294d1-152">-Windows</span></span>
<span data-ttu-id="294d1-153">İşletim sistemi türünün Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="294d1-153">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-154">-Winrmcercertificate Ateurl</span><span class="sxs-lookup"><span data-stu-id="294d1-154">-WinRMCertificateUrl</span></span>
<span data-ttu-id="294d1-155">WinRM sertifikasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="294d1-155">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="294d1-156">Bunun bir Anahtar Kasası içinde depolanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="294d1-156">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-157">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="294d1-157">-WinRMHttp</span></span>
<span data-ttu-id="294d1-158">Bu işletim sisteminin HTTP WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="294d1-158">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-159">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="294d1-159">-WinRMHttps</span></span>
<span data-ttu-id="294d1-160">Bu işletim sisteminin HTTPS WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="294d1-160">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="294d1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294d1-161">CommonParameters</span></span>
<span data-ttu-id="294d1-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="294d1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294d1-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294d1-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294d1-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="294d1-164">INPUTS</span></span>

### <span data-ttu-id="294d1-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="294d1-165">None</span></span>
<span data-ttu-id="294d1-166">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="294d1-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="294d1-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="294d1-167">OUTPUTS</span></span>

## <span data-ttu-id="294d1-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="294d1-168">NOTES</span></span>

## <span data-ttu-id="294d1-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="294d1-169">RELATED LINKS</span></span>

[<span data-ttu-id="294d1-170">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="294d1-170">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="294d1-171">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="294d1-171">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


