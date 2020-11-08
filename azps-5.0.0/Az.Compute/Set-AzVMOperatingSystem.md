---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277493"
---
# <span data-ttu-id="bbf78-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bbf78-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="bbf78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf78-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf78-103">Sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="bbf78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbf78-104">SYNTAX</span></span>

### <span data-ttu-id="bbf78-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbf78-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbf78-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="bbf78-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf78-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="bbf78-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbf78-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="bbf78-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbf78-109">UX</span><span class="sxs-lookup"><span data-stu-id="bbf78-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbf78-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbf78-110">DESCRIPTION</span></span>
<span data-ttu-id="bbf78-111">**Set-AzVMOperatingSystem** cmdlet 'i sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="bbf78-112">Oturum açma kimlik bilgilerini, bilgisayar adını ve işletim sistemi türünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbf78-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="bbf78-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbf78-113">EXAMPLES</span></span>

### <span data-ttu-id="bbf78-114">Örnek 1: yeni sanal makinelerin işletim sistemi özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bbf78-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="bbf78-115">İlk komut, parolayı güvenli bir dizeye dönüştürür ve $SecurePassword değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="bbf78-116">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="bbf78-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="bbf78-117">İkinci komut, Kullanıcı Tamcağı ve $SecurePassword depolanan parola için bir kimlik bilgisi oluşturur ve $Credential değişkeninde kimlik bilgisini depolar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="bbf78-118">Daha fazla bilgi için yazın `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="bbf78-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="bbf78-119">Üçüncü komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="bbf78-120">Dördüncü komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bbf78-121">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bbf78-122">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="bbf78-123">Sonraki dört komut, aşağıdaki komutta kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="bbf78-124">Bu dizeleri doğrudan **set-AzVMOperatingSystem** komutunda belirtebileceğinden, bu yaklaşım yalnızca okunabilirlik için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bbf78-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="bbf78-125">Ancak, komut dosyalarında bu gibi bir yaklaşım kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbf78-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="bbf78-126">Son komut $VirtualMachine depolanan sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bbf78-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bbf78-127">Komut $Credential uygulamasında depolanan kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bbf78-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="bbf78-128">Komut bazı parametrelerde önceki komutlarda atanan değişkenleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="bbf78-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="bbf78-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbf78-129">PARAMETERS</span></span>

### <span data-ttu-id="bbf78-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="bbf78-130">-ComputerName</span></span>
<span data-ttu-id="bbf78-131">Bilgisayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-131">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="bbf78-132">-Credential</span></span>
<span data-ttu-id="bbf78-133">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="bbf78-134">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bbf78-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="bbf78-135">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="bbf78-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="bbf78-136">-CustomData</span></span>
<span data-ttu-id="bbf78-137">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="bbf78-138">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="bbf78-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="bbf78-139">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="bbf78-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="bbf78-140">**Not: customData özelliğinde hiçbir parolayı veya parolayı geçirmeyin**</span><span class="sxs-lookup"><span data-stu-id="bbf78-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="bbf78-141">Bu özellik VM oluşturulduktan sonra güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="bbf78-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="bbf78-142">customData, bir dosya olarak kaydedilmesi için VM 'ye geçirilir, daha fazla bilgi için [Azure VM 'lerle Ilgili özel verilere](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) bakın</span><span class="sxs-lookup"><span data-stu-id="bbf78-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="bbf78-143">Linux VM 'unuzda bulut-init kullanmak için, [oluşturma sırasında bir LINUX VM 'yi özelleştirmek için bulut-Init kullanma](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="bbf78-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf78-144">-DefaultProfile</span></span>
<span data-ttu-id="bbf78-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbf78-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="bbf78-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="bbf78-147">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="bbf78-148">-DisableVMAgent</span></span>
<span data-ttu-id="bbf78-149">VM Aracısı sağlamayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="bbf78-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-150">-Enableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="bbf78-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="bbf78-151">Bu cmdlet 'in otomatik güncelleştirmeyi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="bbf78-152">-Linux</span></span>
<span data-ttu-id="bbf78-153">İşletim sistemi türünün Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="bbf78-154">-PatchMode</span></span>
<span data-ttu-id="bbf78-155">IaaS sanal makinesi ile Konuk içi düzeltme düzeltmesi modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="bbf78-156">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="bbf78-156">Possible values are:</span></span><br>
<span data-ttu-id="bbf78-157">**El ile** -bir sanal makineye düzeltme eklerinin uygulamasını kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbf78-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="bbf78-158">Bu işlemi, sanal makinenin içinde düzeltme eklerini el ile uygulayarak yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbf78-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="bbf78-159">Bu modda otomatik güncelleştirmeler devre dışı bırakılır; Özellik WindowsConfiguration. enableAutomaticUpdates false olmalıdır</span><span class="sxs-lookup"><span data-stu-id="bbf78-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="bbf78-160">**AutomaticByOS** Otomatik olarak sanal makine otomatik olarak güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="bbf78-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="bbf78-161">Özellik WindowsConfiguration. enableAutomaticUpdates doğru olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bbf78-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="bbf78-162">**AutomaticByPlatform** Otomatik olarak sanal makine otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="bbf78-163">Properties provisionVMAgent ve WindowsConfiguration. enableAutomaticUpdates doğru olmalıdır</span><span class="sxs-lookup"><span data-stu-id="bbf78-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="bbf78-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="bbf78-165">Ayarların sanal makinede sanal makine aracısının yüklü olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="bbf78-166">-TimeZone</span></span>
<span data-ttu-id="bbf78-167">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="bbf78-168">Örneğin \" Pasifik standart saati \" .</span><span class="sxs-lookup"><span data-stu-id="bbf78-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="bbf78-169">Olası değerler, [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)tarafından döndürülen saat dilimlerinde [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-170">-VM</span><span class="sxs-lookup"><span data-stu-id="bbf78-170">-VM</span></span>
<span data-ttu-id="bbf78-171">İşletim sistemi özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="bbf78-172">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bbf78-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="bbf78-173">New-AzVMConfig cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bbf78-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="bbf78-174">-Windows</span></span>
<span data-ttu-id="bbf78-175">İşletim sistemi türünün Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-176">-Winrmcercertificate Ateurl</span><span class="sxs-lookup"><span data-stu-id="bbf78-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="bbf78-177">WinRM sertifikasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="bbf78-178">Bunun bir Anahtar Kasası içinde depolanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="bbf78-179">-WinRMHttp</span></span>
<span data-ttu-id="bbf78-180">Bu işletim sisteminin HTTP WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="bbf78-181">-WinRMHttps</span></span>
<span data-ttu-id="bbf78-182">Bu işletim sisteminin HTTPS WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbf78-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf78-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf78-183">CommonParameters</span></span>
<span data-ttu-id="bbf78-184">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbf78-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf78-185">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bbf78-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf78-186">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbf78-186">INPUTS</span></span>

### <span data-ttu-id="bbf78-187">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bbf78-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="bbf78-188">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bbf78-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bbf78-189">System. String</span><span class="sxs-lookup"><span data-stu-id="bbf78-189">System.String</span></span>

### <span data-ttu-id="bbf78-190">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="bbf78-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bbf78-191">System. Uri</span><span class="sxs-lookup"><span data-stu-id="bbf78-191">System.Uri</span></span>

## <span data-ttu-id="bbf78-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbf78-192">OUTPUTS</span></span>

### <span data-ttu-id="bbf78-193">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bbf78-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bbf78-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbf78-194">NOTES</span></span>

## <span data-ttu-id="bbf78-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbf78-195">RELATED LINKS</span></span>

[<span data-ttu-id="bbf78-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bbf78-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bbf78-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bbf78-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


