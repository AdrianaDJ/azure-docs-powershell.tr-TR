---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106064"
---
# <span data-ttu-id="de167-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="de167-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="de167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de167-102">SYNOPSIS</span></span>
<span data-ttu-id="de167-103">Dağıtımın durumunu, yapılandırma ayarlarını veya yükseltme modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="de167-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="de167-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de167-104">SYNTAX</span></span>

### <span data-ttu-id="de167-105">Yükseltilecek</span><span class="sxs-lookup"><span data-stu-id="de167-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="de167-106">Yapılandırmadan</span><span class="sxs-lookup"><span data-stu-id="de167-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="de167-107">Durumları</span><span class="sxs-lookup"><span data-stu-id="de167-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="de167-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="de167-108">DESCRIPTION</span></span>
<span data-ttu-id="de167-109">**Set-AzureDeployment** cmdlet 'ı bir Azure dağıtımının durumunu, yapılandırma ayarlarını veya yükseltme modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="de167-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="de167-110">Dağıtımın durumunu çalışıyor veya askıya alınmış olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de167-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="de167-111">Dağıtımın. cscfg dosyasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de167-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="de167-112">Yükseltme modunu ayarlayabilir ve yapılandırma dosyalarını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de167-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="de167-113">Bir yükseltme başlatmak için **set-AzureWalkUpgradeDomain** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="de167-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="de167-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de167-114">EXAMPLES</span></span>

### <span data-ttu-id="de167-115">Örnek 1: dağıtımın durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="de167-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="de167-116">Bu komut, üretim ortamındaki Contososervisi adlı hizmetin dağıtımını çalıştırması için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="de167-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="de167-117">Örnek 2: dağıtıma farklı bir yapılandırma dosyası atama</span><span class="sxs-lookup"><span data-stu-id="de167-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="de167-118">Bu komut, hazırlama ortamındaki Contosohizmeti adlı hizmetin dağıtımı için farklı bir yapılandırma dosyası atar.</span><span class="sxs-lookup"><span data-stu-id="de167-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="de167-119">Örnek 3: yükseltme modunu otomatik olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="de167-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="de167-120">Bu komut yükseltme modunu otomatik olarak ayarlar ve yükseltme paketini ve yeni yapılandırma dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="de167-121">Örnek 4: bir hizmete uzantı yapılandırması yükleme</span><span class="sxs-lookup"><span data-stu-id="de167-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="de167-122">Bu komut belirtilen bulut hizmetine uzantı yapılandırmasını yükler ve bunları rollerle uygular.</span><span class="sxs-lookup"><span data-stu-id="de167-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="de167-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de167-123">PARAMETERS</span></span>

### <span data-ttu-id="de167-124">-Config</span><span class="sxs-lookup"><span data-stu-id="de167-124">-Config</span></span>
<span data-ttu-id="de167-125">Bu cmdlet 'in dağıtımın yapılandırmasını değiştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-126">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="de167-126">-Configuration</span></span>
<span data-ttu-id="de167-127">. Cscfg yapılandırma dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="de167-128">Yükseltme veya yapılandırma değişikliği için yapılandırma dosyası belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de167-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="de167-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="de167-130">Uzantı yapılandırma nesneleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de167-131">-Force</span><span class="sxs-lookup"><span data-stu-id="de167-131">-Force</span></span>
<span data-ttu-id="de167-132">Cmdlet 'in Zorlanmış yükseltme gerçekleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="de167-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-133">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="de167-133">-InformationAction</span></span>
<span data-ttu-id="de167-134">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="de167-135">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="de167-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="de167-136">'A</span><span class="sxs-lookup"><span data-stu-id="de167-136">Continue</span></span>
- <span data-ttu-id="de167-137">Manıza</span><span class="sxs-lookup"><span data-stu-id="de167-137">Ignore</span></span>
- <span data-ttu-id="de167-138">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="de167-138">Inquire</span></span>
- <span data-ttu-id="de167-139">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="de167-139">SilentlyContinue</span></span>
- <span data-ttu-id="de167-140">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="de167-140">Stop</span></span>
- <span data-ttu-id="de167-141">Biliriz</span><span class="sxs-lookup"><span data-stu-id="de167-141">Suspend</span></span>

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

### <span data-ttu-id="de167-142">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="de167-142">-InformationVariable</span></span>
<span data-ttu-id="de167-143">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="de167-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="de167-144">-Label</span></span>
<span data-ttu-id="de167-145">Yükseltilen dağıtımın etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-146">-Mod</span><span class="sxs-lookup"><span data-stu-id="de167-146">-Mode</span></span>
<span data-ttu-id="de167-147">Yükseltme modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="de167-148">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="de167-148">Valid values are:</span></span> 

- <span data-ttu-id="de167-149">Otomatik</span><span class="sxs-lookup"><span data-stu-id="de167-149">Auto</span></span> 
- <span data-ttu-id="de167-150">El ile</span><span class="sxs-lookup"><span data-stu-id="de167-150">Manual</span></span> 
- <span data-ttu-id="de167-151">Eşzamanlı</span><span class="sxs-lookup"><span data-stu-id="de167-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="de167-152">-NewStatus</span></span>
<span data-ttu-id="de167-153">Dağıtımın hedef durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="de167-154">Geçerli değerler: çalışıyor ve askıya alındı.</span><span class="sxs-lookup"><span data-stu-id="de167-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-155">-Package</span><span class="sxs-lookup"><span data-stu-id="de167-155">-Package</span></span>
<span data-ttu-id="de167-156">Yükseltme paketi dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-157">-Profil</span><span class="sxs-lookup"><span data-stu-id="de167-157">-Profile</span></span>
<span data-ttu-id="de167-158">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="de167-159">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="de167-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="de167-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="de167-160">-RoleName</span></span>
<span data-ttu-id="de167-161">Yükseltilecek rolün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-162">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="de167-162">-ServiceName</span></span>
<span data-ttu-id="de167-163">Dağıtımın Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-163">Specifies the name of the Azure service of the deployment.</span></span>

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

### <span data-ttu-id="de167-164">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="de167-164">-Slot</span></span>
<span data-ttu-id="de167-165">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="de167-166">Geçerli değerler: üretim ve hazırlama.</span><span class="sxs-lookup"><span data-stu-id="de167-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de167-167">-Durum</span><span class="sxs-lookup"><span data-stu-id="de167-167">-Status</span></span>
<span data-ttu-id="de167-168">Bu cmdlet 'in dağıtımın durumunu değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-169">-Yükseltme</span><span class="sxs-lookup"><span data-stu-id="de167-169">-Upgrade</span></span>
<span data-ttu-id="de167-170">Bu cmdlet 'in dağıtımı yükseltmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de167-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de167-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de167-171">CommonParameters</span></span>
<span data-ttu-id="de167-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de167-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de167-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de167-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de167-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de167-174">INPUTS</span></span>

## <span data-ttu-id="de167-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de167-175">OUTPUTS</span></span>

## <span data-ttu-id="de167-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de167-176">NOTES</span></span>

## <span data-ttu-id="de167-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de167-177">RELATED LINKS</span></span>

[<span data-ttu-id="de167-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="de167-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="de167-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="de167-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="de167-180">Taşı-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="de167-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="de167-181">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="de167-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="de167-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="de167-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="de167-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="de167-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


