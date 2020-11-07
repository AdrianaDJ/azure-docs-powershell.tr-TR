---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 874045a510c8ab87143e25994fd5f15d5be7e741
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936825"
---
# <span data-ttu-id="3e72b-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3e72b-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="3e72b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e72b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e72b-103">Sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="3e72b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e72b-104">SYNTAX</span></span>

### <span data-ttu-id="3e72b-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e72b-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e72b-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="3e72b-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e72b-107">UX</span><span class="sxs-lookup"><span data-stu-id="3e72b-107">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e72b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e72b-108">DESCRIPTION</span></span>
<span data-ttu-id="3e72b-109">**Set-AzVMOperatingSystem** cmdlet 'i sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-109">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="3e72b-110">Oturum açma kimlik bilgilerini, bilgisayar adını ve işletim sistemi türünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e72b-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="3e72b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e72b-111">EXAMPLES</span></span>

### <span data-ttu-id="3e72b-112">Örnek 1: yeni sanal makinelerin işletim sistemi özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e72b-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="3e72b-113">İlk komut, parolayı güvenli bir dizeye dönüştürür ve $SecurePassword değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="3e72b-114">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="3e72b-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="3e72b-115">İkinci komut, Kullanıcı Tamcağı ve $SecurePassword depolanan parola için bir kimlik bilgisi oluşturur ve $Credential değişkeninde kimlik bilgisini depolar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="3e72b-116">Daha fazla bilgi için yazın `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="3e72b-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="3e72b-117">Üçüncü komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="3e72b-118">Dördüncü komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="3e72b-119">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="3e72b-120">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="3e72b-121">Sonraki dört komut, aşağıdaki komutta kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="3e72b-122">Bu dizeleri doğrudan **set-AzVMOperatingSystem** komutunda belirtebileceğinden, bu yaklaşım yalnızca okunabilirlik için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e72b-122">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="3e72b-123">Ancak, komut dosyalarında bu gibi bir yaklaşım kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e72b-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="3e72b-124">Son komut $VirtualMachine depolanan sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3e72b-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="3e72b-125">Komut $Credential uygulamasında depolanan kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e72b-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="3e72b-126">Komut bazı parametrelerde önceki komutlarda atanan değişkenleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e72b-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="3e72b-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e72b-127">PARAMETERS</span></span>

### <span data-ttu-id="3e72b-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="3e72b-128">-ComputerName</span></span>
<span data-ttu-id="3e72b-129">Bilgisayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="3e72b-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="3e72b-130">-Credential</span></span>
<span data-ttu-id="3e72b-131">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="3e72b-132">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e72b-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="3e72b-133">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="3e72b-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="3e72b-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="3e72b-134">-CustomData</span></span>
<span data-ttu-id="3e72b-135">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="3e72b-136">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="3e72b-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="3e72b-137">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="3e72b-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="3e72b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e72b-138">-DefaultProfile</span></span>
<span data-ttu-id="3e72b-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e72b-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e72b-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="3e72b-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="3e72b-141">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="3e72b-142">-Enableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3e72b-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="3e72b-143">Bu cmdlet 'in otomatik güncelleştirmeyi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-143">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="3e72b-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="3e72b-144">-Linux</span></span>
<span data-ttu-id="3e72b-145">İşletim sistemi türünün Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="3e72b-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="3e72b-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="3e72b-147">Ayarların sanal makinede sanal makine aracısının yüklü olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="3e72b-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="3e72b-148">-TimeZone</span></span>
<span data-ttu-id="3e72b-149">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-149">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="3e72b-150">-VM</span><span class="sxs-lookup"><span data-stu-id="3e72b-150">-VM</span></span>
<span data-ttu-id="3e72b-151">İşletim sistemi özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="3e72b-152">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e72b-152">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="3e72b-153">New-AzVMConfig cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3e72b-153">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="3e72b-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="3e72b-154">-Windows</span></span>
<span data-ttu-id="3e72b-155">İşletim sistemi türünün Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-155">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="3e72b-156">-Winrmcercertificate Ateurl</span><span class="sxs-lookup"><span data-stu-id="3e72b-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="3e72b-157">WinRM sertifikasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="3e72b-158">Bunun bir Anahtar Kasası içinde depolanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-158">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="3e72b-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="3e72b-159">-WinRMHttp</span></span>
<span data-ttu-id="3e72b-160">Bu işletim sisteminin HTTP WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-160">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="3e72b-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="3e72b-161">-WinRMHttps</span></span>
<span data-ttu-id="3e72b-162">Bu işletim sisteminin HTTPS WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e72b-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="3e72b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e72b-163">CommonParameters</span></span>
<span data-ttu-id="3e72b-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e72b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e72b-165">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e72b-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e72b-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e72b-166">INPUTS</span></span>

### <span data-ttu-id="3e72b-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3e72b-167">PSVirtualMachine</span></span>
<span data-ttu-id="3e72b-168">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="3e72b-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="3e72b-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e72b-169">OUTPUTS</span></span>

### <span data-ttu-id="3e72b-170">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3e72b-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3e72b-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e72b-171">NOTES</span></span>

## <span data-ttu-id="3e72b-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e72b-172">RELATED LINKS</span></span>

[<span data-ttu-id="3e72b-173">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e72b-173">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="3e72b-174">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3e72b-174">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


