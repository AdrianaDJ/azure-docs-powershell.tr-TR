---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105929"
---
# <span data-ttu-id="87021-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="87021-101">New-AzureDeployment</span></span>

## <span data-ttu-id="87021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87021-102">SYNOPSIS</span></span>
<span data-ttu-id="87021-103">Bir hizmetten dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="87021-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87021-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87021-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87021-105">DESCRIPTION</span></span>
<span data-ttu-id="87021-106">**New-AzureDeployment** cmdlet 'i, Web rollerini ve çalışan rollerini içeren hizmetten bir Azure dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="87021-107">Bu cmdlet, paket dosyasına (. cspkg) ve hizmet yapılandırma dosyasına (. cscfg) dayalı bir dağıtım oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="87021-108">Dağıtım ortamında benzersiz bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="87021-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="87021-109">Azure sanal makinelerine dayalı bir dağıtım oluşturmak için **New-AzureVM** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="87021-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="87021-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87021-110">EXAMPLES</span></span>

### <span data-ttu-id="87021-111">Örnek 1: dağıtım oluşturma</span><span class="sxs-lookup"><span data-stu-id="87021-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="87021-112">Bu komut, ContosoPackage. cspkg adındaki paketi ve ContosoConfiguration. cscfg adlı bir yapılandırmayı temel alan bir üretim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="87021-113">Komut, dağıtımın etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="87021-114">Bir ad belirtmez.</span><span class="sxs-lookup"><span data-stu-id="87021-114">It does not specify a name.</span></span>
<span data-ttu-id="87021-115">Bu cmdlet ad olarak bir GUID oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="87021-116">Örnek 2: bir uzantı yapılandırmasına dayalı dağıtım oluşturma</span><span class="sxs-lookup"><span data-stu-id="87021-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="87021-117">Bu komut, pakete ve yapılandırmaya dayalı bir üretim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="87021-118">Komut, ContosoExtensionConfig. cscfg adlı bir uzantı yapılandırması belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="87021-119">Bu cmdlet ad ve etiket olarak GUID 'Ler oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87021-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="87021-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87021-120">PARAMETERS</span></span>

### <span data-ttu-id="87021-121">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="87021-121">-Configuration</span></span>
<span data-ttu-id="87021-122">Hizmet yapılandırma dosyasının tam yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87021-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="87021-123">-DoNotStart</span></span>
<span data-ttu-id="87021-124">Bu cmdlet 'in dağıtımı başlatmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="87021-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="87021-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="87021-126">Uzantı yapılandırma nesneleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87021-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="87021-127">-InformationAction</span></span>
<span data-ttu-id="87021-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87021-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="87021-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87021-130">'A</span><span class="sxs-lookup"><span data-stu-id="87021-130">Continue</span></span>
- <span data-ttu-id="87021-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="87021-131">Ignore</span></span>
- <span data-ttu-id="87021-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="87021-132">Inquire</span></span>
- <span data-ttu-id="87021-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="87021-133">SilentlyContinue</span></span>
- <span data-ttu-id="87021-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="87021-134">Stop</span></span>
- <span data-ttu-id="87021-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="87021-135">Suspend</span></span>

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

### <span data-ttu-id="87021-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="87021-136">-InformationVariable</span></span>
<span data-ttu-id="87021-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87021-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="87021-138">-Label</span></span>
<span data-ttu-id="87021-139">Dağıtım için bir etiket adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="87021-140">Etiket belirtmezseniz, bu cmdlet bir GUID kullanır.</span><span class="sxs-lookup"><span data-stu-id="87021-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87021-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="87021-141">-Name</span></span>
<span data-ttu-id="87021-142">Dağıtım adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-142">Specifies a deployment name.</span></span>
<span data-ttu-id="87021-143">Bir ad belirtmezseniz, bu cmdlet bir GUID kullanır.</span><span class="sxs-lookup"><span data-stu-id="87021-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87021-144">-Package</span><span class="sxs-lookup"><span data-stu-id="87021-144">-Package</span></span>
<span data-ttu-id="87021-145">Aynı aboneliğe veya projeye sahip depolama alanındaki bir. cspkg dosyasının yolunu veya URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87021-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="87021-146">-Profile</span></span>
<span data-ttu-id="87021-147">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87021-148">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="87021-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87021-149">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="87021-149">-ServiceName</span></span>
<span data-ttu-id="87021-150">Dağıtım için Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87021-151">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="87021-151">-Slot</span></span>
<span data-ttu-id="87021-152">Bu cmdlet 'in dağıtımı oluşturduğu ortamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="87021-153">Geçerli değerler: hazırlama ve üretim.</span><span class="sxs-lookup"><span data-stu-id="87021-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="87021-154">Varsayılan değer Production değeridir.</span><span class="sxs-lookup"><span data-stu-id="87021-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87021-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="87021-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="87021-156">Uyarı iletilerinin hata olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="87021-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="87021-157">Bu parametreyi belirtirseniz, dağıtımın başarısız olmasına neden olan bir uyarı iletisi.</span><span class="sxs-lookup"><span data-stu-id="87021-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="87021-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87021-158">CommonParameters</span></span>
<span data-ttu-id="87021-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87021-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87021-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87021-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87021-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87021-161">INPUTS</span></span>

## <span data-ttu-id="87021-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87021-162">OUTPUTS</span></span>

## <span data-ttu-id="87021-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87021-163">NOTES</span></span>

## <span data-ttu-id="87021-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87021-164">RELATED LINKS</span></span>

[<span data-ttu-id="87021-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="87021-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="87021-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="87021-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="87021-167">Taşı-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="87021-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="87021-168">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="87021-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="87021-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="87021-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="87021-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="87021-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


