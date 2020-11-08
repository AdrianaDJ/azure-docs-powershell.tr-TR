---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107351"
---
# <span data-ttu-id="46a23-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46a23-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="46a23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a23-102">SYNOPSIS</span></span>
<span data-ttu-id="46a23-103">Bir sanal makinede DSC uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="46a23-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="46a23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46a23-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46a23-105">DESCRIPTION</span></span>
<span data-ttu-id="46a23-106">**Set-AzureVMDscExtension** cmdlet 'i sanal makinede Istenen durum YAPıLANDıRMASı (DSC) uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="46a23-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="46a23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46a23-107">EXAMPLES</span></span>

### <span data-ttu-id="46a23-108">Örnek 1: sanal makinede DSC uzantısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="46a23-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="46a23-109">Bu komut, bir sanal makinede DSC uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="46a23-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="46a23-110">MyConfiguration.ps1.zip paketi, **Publish-AzureVMDscConfiguration** komutunu kullanarak Azure depolama 'ya daha önce yüklenmiş olmalıdır ve MyConfiguration.ps1 betiğini ve bağımlı olduğu modülleri içerir.</span><span class="sxs-lookup"><span data-stu-id="46a23-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="46a23-111">MyConfiguration bağımsız değişkeni, komut dosyasının yürütüleceği belirli DSC yapılandırmasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46a23-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="46a23-112">- *Configurationargument* parametresi, yapılandırma işlevine iletilen bağımsız değişkenlerle birlikte bir Hashtable belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="46a23-113">Örnek 2: yapılandırma verilerine yol kullanarak sanal makinedeki DSC uzantısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="46a23-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="46a23-114">Bu komut, yapılandırma verilerine yol kullanarak sanal makinedeki DSC uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="46a23-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="46a23-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46a23-115">PARAMETERS</span></span>

### <span data-ttu-id="46a23-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="46a23-116">-ConfigurationArchive</span></span>
<span data-ttu-id="46a23-117">Daha önce Publish-AzureVMDscConfiguration tarafından karşıya yüklenen yapılandırma paketinin (. zip dosyası) adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="46a23-118">Bu parametrenin, herhangi bir yol olmadan yalnızca dosyanın adını belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="46a23-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="46a23-119">-ConfigurationArgument</span></span>
<span data-ttu-id="46a23-120">Yapılandırma işlevinin bağımsız değişkenlerini belirten bir Hashtable belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="46a23-121">Anahtarlar parametre adlarına ve parametre değerlerinin değerlerine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="46a23-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="46a23-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46a23-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46a23-123">ilkel türler</span><span class="sxs-lookup"><span data-stu-id="46a23-123">primitive types</span></span>
- <span data-ttu-id="46a23-124">dizisi</span><span class="sxs-lookup"><span data-stu-id="46a23-124">string</span></span>
- <span data-ttu-id="46a23-125">dizisinde</span><span class="sxs-lookup"><span data-stu-id="46a23-125">array</span></span>
- <span data-ttu-id="46a23-126">Pscrential</span><span class="sxs-lookup"><span data-stu-id="46a23-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="46a23-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="46a23-128">Yapılandırma işlevi için verileri belirten bir. psd1 dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="46a23-129">Bu dosyada, yapılandırma ve ortam verilerini ayırma başlığı altında açıklandığı gibi bir Hashtable bulunmalıdır https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="46a23-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="46a23-130">-ConfigurationName</span></span>
<span data-ttu-id="46a23-131">DSC Uzantısı tarafından çağrılan yapılandırma dosyasının veya modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="46a23-132">Bu parametrenin değeri, *Configurationarchive* 'de paketlenmiş betiklerin veya modüllerdeki bulunan yapılandırma işlevlerinden birinin adı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="46a23-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="46a23-133">Bu cmdlet, herhangi bir uzantıyı dışlayarak, *Configurationarchive* parametresi tarafından verilen dosyanın adını varsayılan olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="46a23-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="46a23-134">Örneğin, *Configurationarchive* "SalesWebSite.ps1.zip" Ise, *ConfigurationName* Için varsayılan değer "satışsitesi" olur.</span><span class="sxs-lookup"><span data-stu-id="46a23-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-135">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="46a23-135">-ContainerName</span></span>
<span data-ttu-id="46a23-136">*Configurationarchive* 'ın bulunduğu Azure depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="46a23-137">-DataCollection</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-138">-Force</span><span class="sxs-lookup"><span data-stu-id="46a23-138">-Force</span></span>
<span data-ttu-id="46a23-139">Bu cmdlet 'in var olan blob 'ları üzerine yaztığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46a23-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-140">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="46a23-140">-InformationAction</span></span>
<span data-ttu-id="46a23-141">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46a23-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46a23-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46a23-143">'A</span><span class="sxs-lookup"><span data-stu-id="46a23-143">Continue</span></span>
- <span data-ttu-id="46a23-144">Manıza</span><span class="sxs-lookup"><span data-stu-id="46a23-144">Ignore</span></span>
- <span data-ttu-id="46a23-145">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="46a23-145">Inquire</span></span>
- <span data-ttu-id="46a23-146">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="46a23-146">SilentlyContinue</span></span>
- <span data-ttu-id="46a23-147">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="46a23-147">Stop</span></span>
- <span data-ttu-id="46a23-148">Biliriz</span><span class="sxs-lookup"><span data-stu-id="46a23-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-149">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="46a23-149">-InformationVariable</span></span>
<span data-ttu-id="46a23-150">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="46a23-151">-Profile</span></span>
<span data-ttu-id="46a23-152">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46a23-153">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="46a23-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="46a23-154">-ReferenceName</span></span>
<span data-ttu-id="46a23-155">Uzantıya başvurmak için kullanılabilecek Kullanıcı tanımlı bir dize belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="46a23-156">Bu parametre, uzantı sanal makineye ilk kez eklendiğinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="46a23-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="46a23-157">Sonraki güncelleştirmelerde, uzantıyı güncelleştirirken önceden kullanılmış başvuru adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="46a23-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="46a23-158">Uzantıya atanan *ReferenceName* , **Get-AzureVM** cmdlet 'i kullanılarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="46a23-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="46a23-159">-StorageContext</span></span>
<span data-ttu-id="46a23-160">Yapılandırma komut dosyasına erişmek için kullanılan güvenlik ayarlarını sağlayan Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="46a23-161">Bu bağlam, *ContainerName* parametresinde belirtilen kapsayıcıya okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="46a23-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="46a23-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="46a23-163">Tüm depolama hizmetleri için DNS uç noktası sonekini (örneğin, "core.contoso.net") belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-164">-Version</span><span class="sxs-lookup"><span data-stu-id="46a23-164">-Version</span></span>
<span data-ttu-id="46a23-165">DSC uzantısının kullanılacak sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="46a23-166">Bu parametre belirtilmemişse varsayılan değer "1. \*" olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="46a23-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-167">-VM</span><span class="sxs-lookup"><span data-stu-id="46a23-167">-VM</span></span>
<span data-ttu-id="46a23-168">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="46a23-169">-WmfVersion</span></span>
<span data-ttu-id="46a23-170">Sanal makineye yüklenecek Windows Yönetim çerçevesi (WMF) sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="46a23-171">DSC Uzantısı, yalnızca WMF güncelleştirmelerinde bulunan DSC özelliklerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="46a23-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="46a23-172">Bu parametre, güncelleştirmenin hangi sürümünün sanal makineye yükleneceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46a23-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="46a23-173">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46a23-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46a23-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="46a23-174">4.0.</span></span>
<span data-ttu-id="46a23-175">Daha yeni bir sürüm yüklü değilse, WMF 4,0 'i yükler.</span><span class="sxs-lookup"><span data-stu-id="46a23-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="46a23-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="46a23-176">5.0.</span></span>
<span data-ttu-id="46a23-177">WMF 5,0 'in en son sürümünü yükler.</span><span class="sxs-lookup"><span data-stu-id="46a23-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="46a23-178">sürümü.</span><span class="sxs-lookup"><span data-stu-id="46a23-178">latest.</span></span>
<span data-ttu-id="46a23-179">En son WMF, şu anda WMF 5,0 yükler.</span><span class="sxs-lookup"><span data-stu-id="46a23-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="46a23-180">Varsayılan değer en son olur.</span><span class="sxs-lookup"><span data-stu-id="46a23-180">The default value is latest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="46a23-181">-Confirm</span></span>
<span data-ttu-id="46a23-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46a23-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a23-183">-WhatIf</span></span>
<span data-ttu-id="46a23-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46a23-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a23-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46a23-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a23-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a23-186">CommonParameters</span></span>
<span data-ttu-id="46a23-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46a23-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a23-188">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a23-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a23-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46a23-189">INPUTS</span></span>

## <span data-ttu-id="46a23-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46a23-190">OUTPUTS</span></span>

## <span data-ttu-id="46a23-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46a23-191">NOTES</span></span>

## <span data-ttu-id="46a23-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46a23-192">RELATED LINKS</span></span>

[<span data-ttu-id="46a23-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46a23-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="46a23-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46a23-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="46a23-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="46a23-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="46a23-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="46a23-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="46a23-197">Yayımla-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a23-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


