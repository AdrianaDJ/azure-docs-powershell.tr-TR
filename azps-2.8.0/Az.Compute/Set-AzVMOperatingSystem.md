---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 60c5d9326b99c8349554f8b3eff2a432382c018e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752677"
---
# <span data-ttu-id="ba7e2-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ba7e2-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="ba7e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7e2-103">Sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="ba7e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba7e2-104">SYNTAX</span></span>

### <span data-ttu-id="ba7e2-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba7e2-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7e2-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ba7e2-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7e2-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="ba7e2-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7e2-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ba7e2-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7e2-109">UX</span><span class="sxs-lookup"><span data-stu-id="ba7e2-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba7e2-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba7e2-110">DESCRIPTION</span></span>
<span data-ttu-id="ba7e2-111">**Set-AzVMOperatingSystem** cmdlet 'i sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="ba7e2-112">Oturum açma kimlik bilgilerini, bilgisayar adını ve işletim sistemi türünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="ba7e2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba7e2-113">EXAMPLES</span></span>

### <span data-ttu-id="ba7e2-114">Örnek 1: yeni sanal makinelerin işletim sistemi özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="ba7e2-114">Example 1: Set operating system properties for a new virtual machines</span></span>
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

<span data-ttu-id="ba7e2-115">İlk komut, parolayı güvenli bir dizeye dönüştürür ve $SecurePassword değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="ba7e2-116">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ba7e2-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="ba7e2-117">İkinci komut, Kullanıcı Tamcağı ve $SecurePassword depolanan parola için bir kimlik bilgisi oluşturur ve $Credential değişkeninde kimlik bilgisini depolar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="ba7e2-118">Daha fazla bilgi için yazın `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="ba7e2-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="ba7e2-119">Üçüncü komut, ResourceGroup11 adındaki kaynak grubundaki AvailabilitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ba7e2-120">Dördüncü komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ba7e2-121">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ba7e2-122">Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ba7e2-123">Sonraki dört komut, aşağıdaki komutta kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="ba7e2-124">Bu dizeleri doğrudan **set-AzVMOperatingSystem** komutunda belirtebileceğinden, bu yaklaşım yalnızca okunabilirlik için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="ba7e2-125">Ancak, komut dosyalarında bu gibi bir yaklaşım kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="ba7e2-126">Son komut $VirtualMachine depolanan sanal makinenin işletim sistemi özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ba7e2-127">Komut $Credential uygulamasında depolanan kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="ba7e2-128">Komut bazı parametrelerde önceki komutlarda atanan değişkenleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="ba7e2-129">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba7e2-129">PARAMETERS</span></span>

### <span data-ttu-id="ba7e2-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ba7e2-130">-ComputerName</span></span>
<span data-ttu-id="ba7e2-131">Bilgisayarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="ba7e2-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="ba7e2-132">-Credential</span></span>
<span data-ttu-id="ba7e2-133">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ba7e2-134">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ba7e2-135">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ba7e2-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="ba7e2-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ba7e2-136">-CustomData</span></span>
<span data-ttu-id="ba7e2-137">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ba7e2-138">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ba7e2-139">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ba7e2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7e2-140">-DefaultProfile</span></span>
<span data-ttu-id="ba7e2-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba7e2-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ba7e2-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ba7e2-143">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="ba7e2-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="ba7e2-144">-DisableVMAgent</span></span>
<span data-ttu-id="ba7e2-145">VM Aracısı sağlamayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="ba7e2-146">-Enableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ba7e2-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="ba7e2-147">Bu cmdlet 'in otomatik güncelleştirmeyi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="ba7e2-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="ba7e2-148">-Linux</span></span>
<span data-ttu-id="ba7e2-149">İşletim sistemi türünün Linux olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="ba7e2-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ba7e2-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="ba7e2-151">Ayarların sanal makinede sanal makine aracısının yüklü olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="ba7e2-152">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ba7e2-152">-TimeZone</span></span>
<span data-ttu-id="ba7e2-153">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="ba7e2-154">-VM</span><span class="sxs-lookup"><span data-stu-id="ba7e2-154">-VM</span></span>
<span data-ttu-id="ba7e2-155">İşletim sistemi özelliklerini ayarlanacak yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="ba7e2-156">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-156">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ba7e2-157">New-AzVMConfig cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-157">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="ba7e2-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="ba7e2-158">-Windows</span></span>
<span data-ttu-id="ba7e2-159">İşletim sistemi türünün Windows olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="ba7e2-160">-Winrmcercertificate Ateurl</span><span class="sxs-lookup"><span data-stu-id="ba7e2-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="ba7e2-161">WinRM sertifikasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="ba7e2-162">Bunun bir Anahtar Kasası içinde depolanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="ba7e2-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ba7e2-163">-WinRMHttp</span></span>
<span data-ttu-id="ba7e2-164">Bu işletim sisteminin HTTP WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="ba7e2-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ba7e2-165">-WinRMHttps</span></span>
<span data-ttu-id="ba7e2-166">Bu işletim sisteminin HTTPS WinRM kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="ba7e2-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7e2-167">CommonParameters</span></span>
<span data-ttu-id="ba7e2-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7e2-169">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba7e2-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7e2-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba7e2-170">INPUTS</span></span>

### <span data-ttu-id="ba7e2-171">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ba7e2-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ba7e2-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba7e2-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ba7e2-173">System. String</span><span class="sxs-lookup"><span data-stu-id="ba7e2-173">System.String</span></span>

### <span data-ttu-id="ba7e2-174">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ba7e2-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="ba7e2-175">System. Uri</span><span class="sxs-lookup"><span data-stu-id="ba7e2-175">System.Uri</span></span>

## <span data-ttu-id="ba7e2-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba7e2-176">OUTPUTS</span></span>

### <span data-ttu-id="ba7e2-177">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ba7e2-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ba7e2-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba7e2-178">NOTES</span></span>

## <span data-ttu-id="ba7e2-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba7e2-179">RELATED LINKS</span></span>

[<span data-ttu-id="ba7e2-180">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ba7e2-180">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ba7e2-181">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ba7e2-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


