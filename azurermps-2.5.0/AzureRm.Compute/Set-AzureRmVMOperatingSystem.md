---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmoperatingsystem
schema: 2.0.0
ms.openlocfilehash: 0eea5d3a4f379b61e5d66e04b66e7812abaf75f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939931"
---
# <span data-ttu-id="463fd-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="463fd-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="463fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="463fd-102">SYNOPSIS</span></span>
<span data-ttu-id="463fd-103">Sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="463fd-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="463fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="463fd-104">SYNTAX</span></span>

### <span data-ttu-id="463fd-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="463fd-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463fd-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="463fd-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463fd-107">UX</span><span class="sxs-lookup"><span data-stu-id="463fd-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="463fd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="463fd-108">DESCRIPTION</span></span>
<span data-ttu-id="463fd-109">**Set-AzureRmVMOperatingSystem** cmdlet 'i sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="463fd-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="463fd-110">Oturum açma kimlik bilgilerini, bilgisayar adını ve işletim sistemi türünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="463fd-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="463fd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="463fd-111">EXAMPLES</span></span>

### <span data-ttu-id="463fd-112">Örnek 1: yeni sanal makinelerin işletim sistemi özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="463fd-112">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="463fd-113">İlk komut, parolayı güvenli bir dizeye dönüştürür ve $SecurePassword değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="463fd-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="463fd-114">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="463fd-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="463fd-115">İkinci komut, Kullanıcı Tamcağı ve $SecurePassword depolanan parola için bir kimlik bilgisi oluşturur ve $Credential değişkeninde kimlik bilgisini depolar.</span><span class="sxs-lookup"><span data-stu-id="463fd-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="463fd-116">Daha fazla bilgi için yazın `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="463fd-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="463fd-117">Üçüncü komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="463fd-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="463fd-118">Dördüncü komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="463fd-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="463fd-119">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="463fd-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="463fd-120">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="463fd-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="463fd-121">Sonraki dört komut, aşağıdaki komutta kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="463fd-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="463fd-122">Bu dizeleri doğrudan **set-AzureRmVMOperatingSystem** komutunda belirtebileceğinden, bu yaklaşım yalnızca okunabilirlik için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="463fd-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="463fd-123">Ancak, komut dosyalarında bu gibi bir yaklaşım kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="463fd-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="463fd-124">Son komut $VirtualMachine depolanan sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="463fd-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="463fd-125">Komut $Credential uygulamasında depolanan kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="463fd-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="463fd-126">Komut bazı parametrelerde önceki komutlarda atanan değişkenleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="463fd-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="463fd-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="463fd-127">PARAMETERS</span></span>

### <span data-ttu-id="463fd-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="463fd-128">-ComputerName</span></span>
<span data-ttu-id="463fd-129">Bilgisayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-129">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="463fd-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="463fd-130">-Credential</span></span>
<span data-ttu-id="463fd-131">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="463fd-132">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="463fd-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="463fd-133">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="463fd-133">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="463fd-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="463fd-134">-CustomData</span></span>
<span data-ttu-id="463fd-135">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="463fd-136">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="463fd-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="463fd-137">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="463fd-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="463fd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463fd-138">-DefaultProfile</span></span>
<span data-ttu-id="463fd-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="463fd-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="463fd-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="463fd-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="463fd-141">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="463fd-141">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="463fd-142">-Enableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="463fd-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="463fd-143">Bu cmdlet 'in otomatik güncelleştirmeyi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="463fd-143">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="463fd-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="463fd-144">-Linux</span></span>
<span data-ttu-id="463fd-145">İşletim sistemi türünün Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="463fd-145">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="463fd-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="463fd-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="463fd-147">Ayarların sanal makinede sanal makine aracısının yüklü olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="463fd-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="463fd-148">-TimeZone</span></span>
<span data-ttu-id="463fd-149">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-149">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="463fd-150">-VM</span><span class="sxs-lookup"><span data-stu-id="463fd-150">-VM</span></span>
<span data-ttu-id="463fd-151">İşletim sistemi özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="463fd-152">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="463fd-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="463fd-153">New-AzureRmVMConfig cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="463fd-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="463fd-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="463fd-154">-Windows</span></span>
<span data-ttu-id="463fd-155">İşletim sistemi türünün Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="463fd-155">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="463fd-156">-Winrmcercertificate Ateurl</span><span class="sxs-lookup"><span data-stu-id="463fd-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="463fd-157">WinRM sertifikasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="463fd-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="463fd-158">Bunun bir Anahtar Kasası içinde depolanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="463fd-158">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="463fd-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="463fd-159">-WinRMHttp</span></span>
<span data-ttu-id="463fd-160">Bu işletim sisteminin HTTP WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="463fd-160">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="463fd-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="463fd-161">-WinRMHttps</span></span>
<span data-ttu-id="463fd-162">Bu işletim sisteminin HTTPS WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="463fd-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="463fd-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463fd-163">CommonParameters</span></span>
<span data-ttu-id="463fd-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="463fd-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463fd-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463fd-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463fd-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="463fd-166">INPUTS</span></span>

### <span data-ttu-id="463fd-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="463fd-167">PSVirtualMachine</span></span>
<span data-ttu-id="463fd-168">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="463fd-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="463fd-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="463fd-169">OUTPUTS</span></span>

### <span data-ttu-id="463fd-170">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="463fd-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="463fd-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="463fd-171">NOTES</span></span>

## <span data-ttu-id="463fd-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="463fd-172">RELATED LINKS</span></span>

[<span data-ttu-id="463fd-173">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="463fd-173">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="463fd-174">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="463fd-174">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


