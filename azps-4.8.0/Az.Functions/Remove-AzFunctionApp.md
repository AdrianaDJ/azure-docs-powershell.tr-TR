---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionApp.md
ms.openlocfilehash: c12c5e3b3f9b8d0ec172b8a2f53951e5a11a0d9b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267699"
---
# <span data-ttu-id="55a60-101">Remove-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="55a60-101">Remove-AzFunctionApp</span></span>

## <span data-ttu-id="55a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a60-102">SYNOPSIS</span></span>
<span data-ttu-id="55a60-103">İşlev uygulaması siler.</span><span class="sxs-lookup"><span data-stu-id="55a60-103">Deletes a function app.</span></span>

## <span data-ttu-id="55a60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55a60-104">SYNTAX</span></span>

### <span data-ttu-id="55a60-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55a60-105">ByName (Default)</span></span>
```
Remove-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="55a60-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="55a60-106">ByObjectInput</span></span>
```
Remove-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55a60-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55a60-107">DESCRIPTION</span></span>
<span data-ttu-id="55a60-108">İşlev uygulaması siler.</span><span class="sxs-lookup"><span data-stu-id="55a60-108">Deletes a function app.</span></span>

## <span data-ttu-id="55a60-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55a60-109">EXAMPLES</span></span>

### <span data-ttu-id="55a60-110">Örnek 1: ada göre bir işlev uygulaması alın ve silin.</span><span class="sxs-lookup"><span data-stu-id="55a60-110">Example 1: Get a function app by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionApp -Force
```

<span data-ttu-id="55a60-111">Bu komut bir işlev uygulamasını adıyla alır ve siler.</span><span class="sxs-lookup"><span data-stu-id="55a60-111">This command gets a function app by name and delete it.</span></span>

### <span data-ttu-id="55a60-112">Örnek 2: ada göre bir işlev uygulaması silme.</span><span class="sxs-lookup"><span data-stu-id="55a60-112">Example 2: Delete a function app by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="55a60-113">Bu komut bir işlev uygulamasını adıyla siler.</span><span class="sxs-lookup"><span data-stu-id="55a60-113">This command deletes a function app by name.</span></span>

## <span data-ttu-id="55a60-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55a60-114">PARAMETERS</span></span>

### <span data-ttu-id="55a60-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a60-115">-DefaultProfile</span></span>
<span data-ttu-id="55a60-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55a60-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-117">-Force</span><span class="sxs-lookup"><span data-stu-id="55a60-117">-Force</span></span>
<span data-ttu-id="55a60-118">Cmdlet 'i, onay istemeden işlev uygulamasını kaldırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-118">Forces the cmdlet to remove the function app without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55a60-119">-InputObject</span></span>
<span data-ttu-id="55a60-120">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="55a60-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="55a60-121">-Name</span></span>
<span data-ttu-id="55a60-122">İşlev uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="55a60-123">-PassThru</span></span>
<span data-ttu-id="55a60-124">Komut başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="55a60-124">Returns true when the command succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a60-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="55a60-126">-SubscriptionId</span></span>
<span data-ttu-id="55a60-127">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="55a60-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="55a60-128">-Confirm</span></span>
<span data-ttu-id="55a60-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55a60-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55a60-130">-WhatIf</span></span>
<span data-ttu-id="55a60-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55a60-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a60-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55a60-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55a60-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a60-133">CommonParameters</span></span>
<span data-ttu-id="55a60-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55a60-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a60-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55a60-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a60-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55a60-136">INPUTS</span></span>

### <span data-ttu-id="55a60-137">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="55a60-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="55a60-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55a60-138">OUTPUTS</span></span>

### <span data-ttu-id="55a60-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55a60-139">System.Boolean</span></span>

## <span data-ttu-id="55a60-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55a60-140">NOTES</span></span>

<span data-ttu-id="55a60-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="55a60-141">ALIASES</span></span>

<span data-ttu-id="55a60-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="55a60-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55a60-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="55a60-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55a60-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55a60-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55a60-145">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="55a60-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="55a60-146">`Location <String>`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="55a60-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="55a60-147">`CloningInfoSourceWebAppId <String>`: Kaynak uygulamanın ARM kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="55a60-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="55a60-148">Uygulama kaynak KIMLIĞI, diğer yuvalarda üretim yuvaları ve/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} için/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} form.</span><span class="sxs-lookup"><span data-stu-id="55a60-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="55a60-149">`[Kind <String>]`: Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="55a60-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="55a60-150">`[Tag <IResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="55a60-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="55a60-151">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55a60-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="55a60-152">`[ClientAffinityEnabled <Boolean?>]`: istemci <code>true</code> benzeşimini etkinleştirmek için; <code>false</code> istemci isteklerini aynı aynı aynı oturumda yönlendiren oturum benzeşimi tanımlama bilgilerini göndermeyi durdurmak için.</span><span class="sxs-lookup"><span data-stu-id="55a60-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="55a60-153">Varsayılan <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="55a60-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> istemci sertifikası kimlik doğrulamasını etkinleştirmek için (TLS karşılıklı kimlik doğrulaması); Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="55a60-155">Varsayılan <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="55a60-156">`[ClientCertExclusionPath <String>]`: istemci sertifikası kimlik doğrulaması virgülle ayrılmış dışlama yolları</span><span class="sxs-lookup"><span data-stu-id="55a60-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="55a60-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Kopyalanan uygulama için uygulama ayarı geçersiz kılmaları.</span><span class="sxs-lookup"><span data-stu-id="55a60-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="55a60-158">Belirtilmişse, bu ayarlar kaynak uygulamadan kopyalanan ayarları geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="55a60-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="55a60-159">Aksi takdirde, kaynak uygulamadaki uygulama ayarları korunur.</span><span class="sxs-lookup"><span data-stu-id="55a60-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="55a60-160">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55a60-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="55a60-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> kaynak uygulamadan özel konak adları kopyalamak için; Aksi halde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="55a60-162">`[CloningInfoCloneSourceControl <Boolean?>]`: kaynak <code>true</code> uygulamayı kaynak uygulamadan kopyalamak için; Aksi halde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="55a60-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> kaynak ve hedef uygulama için yük dengelemeyi yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="55a60-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="55a60-164">`[CloningInfoCorrelationId <String>]`: Kopyalama işleminin bağıntı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="55a60-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="55a60-165">Bu KIMLIK birden çok klonlama işlemini aynı anlık görüntüyü kullanacak şekilde bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="55a60-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="55a60-166">`[CloningInfoHostingEnvironment <String>]`: App Service ortamı.</span><span class="sxs-lookup"><span data-stu-id="55a60-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="55a60-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> hedef uygulamanın üzerine yazmak için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="55a60-168">`[CloningInfoSourceWebAppLocation <String>]`: Kaynak uygulama EX 'ın konumu: Batı ABD veya Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="55a60-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="55a60-169">`[CloningInfoTrafficManagerProfileId <String>]`: Varsa, kullanılacak Traffic Manager profilinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="55a60-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="55a60-170">Traffic Manager kaynak KIMLIĞI/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="55a60-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="55a60-171">`[CloningInfoTrafficManagerProfileName <String>]`: Oluşturulacak Traffic Manager profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="55a60-172">Bu yalnızca Traffic Manager profili yoksa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="55a60-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="55a60-173">`[Config <ISiteConfig>]`: Uygulamanın yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="55a60-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="55a60-174">`IsPushEnabled <Boolean>`: Itme uç noktasının etkinleştirilip etkinleştirilmediğini belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="55a60-175">`[ActionMinProcessExecutionTime <String>]`: İşlemin önüne geçmeden önce işlemin yürütülmesi gereken minimum süre</span><span class="sxs-lookup"><span data-stu-id="55a60-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="55a60-176">`[ActionType <AutoHealActionType?>]`: Önceden tanımlanmış eylem gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="55a60-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="55a60-177">`[AlwaysOn <Boolean?>]`: <code>true</code> her zaman açık etkinleştirilirse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-178">`[ApiDefinitionUrl <String>]`: API tanımının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="55a60-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="55a60-179">`[ApiManagementConfigId <String>]`: APIM-Api tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="55a60-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="55a60-180">`[AppCommandLine <String>]`: Başlatılacak uygulama komut satırı.</span><span class="sxs-lookup"><span data-stu-id="55a60-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="55a60-181">`[AppSetting <INameValuePair[]>]`: Uygulama ayarları.</span><span class="sxs-lookup"><span data-stu-id="55a60-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="55a60-182">`[Name <String>]`: Çift adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="55a60-183">`[Value <String>]`: Çift değer.</span><span class="sxs-lookup"><span data-stu-id="55a60-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="55a60-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Otomatik Heal etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-185">`[AutoSwapSlotName <String>]`: Yuva adı otomatik takas et.</span><span class="sxs-lookup"><span data-stu-id="55a60-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="55a60-186">`[ConnectionString <IConnStringInfo[]>]`: Bağlantı dizeleri.</span><span class="sxs-lookup"><span data-stu-id="55a60-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="55a60-187">`[ConnectionString <String>]`: Bağlantı dizesi değeri.</span><span class="sxs-lookup"><span data-stu-id="55a60-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="55a60-188">`[Name <String>]`: Bağlantı dizesinin adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="55a60-189">`[Type <ConnectionStringType?>]`: Veritabanı türü.</span><span class="sxs-lookup"><span data-stu-id="55a60-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="55a60-190">`[CorAllowedOrigin <String[]>]`: Çapraz kaynak çağrıları yapmasına izin verilmesi gereken kaynak listesini alır veya ayarlar (örneğin: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="55a60-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="55a60-191">Tümüne izin vermek için "\*" kullanın.</span><span class="sxs-lookup"><span data-stu-id="55a60-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="55a60-192">`[CorSupportCredentials <Boolean?>]`: Kimlik bilgilerinin bulunduğu CORS isteklerine izin verilip verilmediğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="55a60-193"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="55a60-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="55a60-194">`[CustomActionExe <String>]`: Çalıştırılabilir dosya.</span><span class="sxs-lookup"><span data-stu-id="55a60-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="55a60-195">`[CustomActionParameter <String>]`: Çalıştırılabilirin parametreleri.</span><span class="sxs-lookup"><span data-stu-id="55a60-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="55a60-196">`[DefaultDocument <String[]>]`: Varsayılan belgeler.</span><span class="sxs-lookup"><span data-stu-id="55a60-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="55a60-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ayrıntılı hata günlüğü etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-198">`[DocumentRoot <String>]`: Belge kökü.</span><span class="sxs-lookup"><span data-stu-id="55a60-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="55a60-199">`[DynamicTagsJson <String>]`: İtme kaydı uç noktasındaki Kullanıcı taleplerini değerlendirilecek dinamik etiket listesini içeren bir JSON dizesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="55a60-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: Rampa kuralları listesi.</span><span class="sxs-lookup"><span data-stu-id="55a60-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="55a60-201">`[ActionHostName <String>]`: Karar verirse trafiğin yönlendirileceği bir yuvanın ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="55a60-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="55a60-202">Yani.</span><span class="sxs-lookup"><span data-stu-id="55a60-202">E.g.</span></span> <span data-ttu-id="55a60-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="55a60-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="55a60-204">`[ChangeDecisionCallbackUrl <String>]`: Özel karar algoritması, TiPCallback site uzantısında hangi URL belirtibileceğine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="55a60-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="55a60-205">Scaffold ve sözleşmeler için TiPCallback site uzantısına bakın.</span><span class="sxs-lookup"><span data-stu-id="55a60-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="55a60-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="55a60-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="55a60-207">`[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="55a60-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="55a60-208">`[ChangeStep <Double?>]`: Otomatik artırma senaryosunda, bu, <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> veya         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="55a60-209">Site ölçümleri, her N dakikada bir işaretlenmelidir <code>ChangeIntervalInMinutes</code> . \nözel karar algoritması, Ýpucu <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="55a60-210">`[MaxReroutePercentage <Double?>]`: ReroutePercentage 'in hangi üst sınıra kalacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a60-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="55a60-211">`[MinReroutePercentage <Double?>]`: ReroutePercentage 'in üzerinde kalacağı alt sınırı belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a60-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="55a60-212">`[Name <String>]`: Yönlendirme kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="55a60-213">Önerilen ad, denemeler sırasında trafiği alacak olan yuvanın üzerine gelmek olacaktır.</span><span class="sxs-lookup"><span data-stu-id="55a60-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="55a60-214">`[ReroutePercentage <Double?>]`: Yönlendirileceği trafiğin yüzdesi <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="55a60-215">`[FtpsState <FtpsState?>]`: FTP/FTPS hizmetinin durumu</span><span class="sxs-lookup"><span data-stu-id="55a60-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="55a60-216">`[HandlerMapping <IHandlerMapping[]>]`: İşleyici eşlemeleri.</span><span class="sxs-lookup"><span data-stu-id="55a60-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="55a60-217">`[Argument <String>]`: Betik işlemcisine geçirilecek komut satırı bağımsız değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="55a60-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="55a60-218">`[Extension <String>]`: Bu uzantıya sahip istekler belirtilen FastCGI uygulaması kullanılarak işlenecek.</span><span class="sxs-lookup"><span data-stu-id="55a60-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="55a60-219">`[ScriptProcessor <String>]`: FastCGI uygulamasının mutlak yolu.</span><span class="sxs-lookup"><span data-stu-id="55a60-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="55a60-220">`[HealthCheckPath <String>]`: Sağlık denetleme yolu</span><span class="sxs-lookup"><span data-stu-id="55a60-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="55a60-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: istemcilerin http 2.0 üzerinden bağlanmasına olanak tanımak için bir Web sitesi yapılandırır</span><span class="sxs-lookup"><span data-stu-id="55a60-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="55a60-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> http günlüğü etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Main için IP güvenlik kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="55a60-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="55a60-224">`[Action <String>]`: Bu IP aralığına erişim izni verin veya erişimi reddedin.</span><span class="sxs-lookup"><span data-stu-id="55a60-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="55a60-225">`[Description <String>]`: IP kısıtlama kuralı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="55a60-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="55a60-226">`[IPAddress <String>]`: IP adresi güvenlik kısıtlamasının geçerlilik olduğu.</span><span class="sxs-lookup"><span data-stu-id="55a60-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="55a60-227">Saf IPv4 adresi (gerekli AltAğMaskesi özelliği) veya IPv4/maske (önde gelen bit eşleşmesi) gibi CıDR gösterimi biçiminde olabilir.</span><span class="sxs-lookup"><span data-stu-id="55a60-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="55a60-228">CıDR için AltAğMaskesi özelliği belirtilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="55a60-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="55a60-229">`[Name <String>]`: IP kısıtlama kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="55a60-230">`[Priority <Int32?>]`: IP kısıtlama kuralının önceliği.</span><span class="sxs-lookup"><span data-stu-id="55a60-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="55a60-231">`[SubnetMask <String>]`: Kısıtlamanın geçerli olduğu IP adresi aralığı için alt ağ maskesi.</span><span class="sxs-lookup"><span data-stu-id="55a60-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="55a60-232">`[SubnetTrafficTag <Int32?>]`: (iç) alt ağ trafiği etiketi</span><span class="sxs-lookup"><span data-stu-id="55a60-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="55a60-233">`[Tag <IPFilterTag?>]`: Bu IP Filtresinin hangi şekilde kullanılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="55a60-234">Bu, proxy 'lerde IP filtrelemesinin desteklenmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="55a60-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="55a60-235">`[VnetSubnetResourceId <String>]`: Sanal ağ kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="55a60-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="55a60-236">`[VnetTrafficTag <Int32?>]`: (iç) VNET trafiği etiketi</span><span class="sxs-lookup"><span data-stu-id="55a60-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="55a60-237">`[JavaContainer <String>]`: Java kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="55a60-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="55a60-238">`[JavaContainerVersion <String>]`: Java kapsayıcı sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="55a60-239">`[JavaVersion <String>]`: Java sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="55a60-240">`[LimitMaxDiskSizeInMb <Int64?>]`: İzin verilen maksimum MB cinsinden disk boyutu kullanımı.</span><span class="sxs-lookup"><span data-stu-id="55a60-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="55a60-241">`[LimitMaxMemoryInMb <Int64?>]`: MB cinsinden izin verilen en fazla bellek kullanımı.</span><span class="sxs-lookup"><span data-stu-id="55a60-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="55a60-242">`[LimitMaxPercentageCpu <Double?>]`: İzin verilen en yüksek CPU kullanımı yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="55a60-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="55a60-243">`[LinuxFxVersion <String>]`: Linux uygulama çerçevesi ve sürümü</span><span class="sxs-lookup"><span data-stu-id="55a60-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="55a60-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site yük dengelemesi.</span><span class="sxs-lookup"><span data-stu-id="55a60-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="55a60-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> Yerel MySQL 'yı etkinleştirmek için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP günlükleri Dizin boyutu sınırını aşıyor.</span><span class="sxs-lookup"><span data-stu-id="55a60-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="55a60-247">`[MachineKeyDecryption <String>]`: Şifre çözme için kullanılan algoritma.</span><span class="sxs-lookup"><span data-stu-id="55a60-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="55a60-248">`[MachineKeyDecryptionKey <String>]`: Şifre çözme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="55a60-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="55a60-249">`[MachineKeyValidation <String>]`: MachineKey doğrulama.</span><span class="sxs-lookup"><span data-stu-id="55a60-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="55a60-250">`[MachineKeyValidationKey <String>]`: Geçerlilik anahtarı.</span><span class="sxs-lookup"><span data-stu-id="55a60-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="55a60-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Yönetilen ardışık düzen modu.</span><span class="sxs-lookup"><span data-stu-id="55a60-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="55a60-252">`[ManagedServiceIdentityId <Int32?>]`: Yönetilen hizmet kimliği kimliği</span><span class="sxs-lookup"><span data-stu-id="55a60-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="55a60-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL istekleri için gereken en düşük TLS sürümünü yapılandırır</span><span class="sxs-lookup"><span data-stu-id="55a60-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="55a60-254">`[NetFrameworkVersion <String>]`: .NET Framework sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="55a60-255">`[NodeVersion <String>]`: Node.js sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="55a60-256">`[NumberOfWorker <Int32?>]`: Çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="55a60-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="55a60-257">`[PhpVersion <String>]`: PHP sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="55a60-258">`[PowerShellVersion <String>]`: PowerShell sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="55a60-259">`[PreWarmedInstanceCount <Int32?>]`: Ön ödeme örneklerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="55a60-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="55a60-260">Bu ayar yalnızca tüketim ve esnek planlar için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="55a60-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="55a60-261">`[PublishingUsername <String>]`: Kullanıcı adı yayımlanıyor.</span><span class="sxs-lookup"><span data-stu-id="55a60-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="55a60-262">`[PushKind <String>]`: Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="55a60-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="55a60-263">`[PythonVersion <String>]`: Python sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="55a60-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Uzaktan hata ayıklama etkinse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-265">`[RemoteDebuggingVersion <String>]`: Uzaktan hata ayıklama sürümü.</span><span class="sxs-lookup"><span data-stu-id="55a60-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="55a60-266">`[RequestCount <Int32?>]`: İstek sayısı.</span><span class="sxs-lookup"><span data-stu-id="55a60-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="55a60-267">`[RequestTimeInterval <String>]`: Zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="55a60-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="55a60-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> istek izleme etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-269">`[RequestTracingExpirationTime <DateTime?>]`: İstek izleme süre sonu.</span><span class="sxs-lookup"><span data-stu-id="55a60-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="55a60-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: SCM için IP güvenlik kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="55a60-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="55a60-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: SCM 'nin Main kullanması için IP güvenlik kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="55a60-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="55a60-272">`[ScmType <ScmType?>]`: SCM türü.</span><span class="sxs-lookup"><span data-stu-id="55a60-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="55a60-273">`[SlowRequestCount <Int32?>]`: İstek sayısı.</span><span class="sxs-lookup"><span data-stu-id="55a60-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="55a60-274">`[SlowRequestTimeInterval <String>]`: Zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="55a60-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="55a60-275">`[SlowRequestTimeTaken <String>]`: Geçen süre.</span><span class="sxs-lookup"><span data-stu-id="55a60-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="55a60-276">`[TagWhitelistJson <String>]`: İtme kaydı uç noktası tarafından kullanılmak üzere, beyaz listelenen etiket listesini içeren bir JSON dizesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="55a60-277">`[TagsRequiringAuth <String>]`: İtme kaydı uç noktasında kullanılacak kullanıcı kimlik doğrulaması gerektiren etiket listesini içeren bir JSON dizesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="55a60-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="55a60-278">Etiketler alfasayısal karakterler ve aşağıdakiler: ' _ ', ' @ ', ' # ', '. ', ': ', '-'.</span><span class="sxs-lookup"><span data-stu-id="55a60-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="55a60-279">Doğrulama, PushRequestHandler ' de gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="55a60-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="55a60-280">`[TracingOption <String>]`: İzleme seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="55a60-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="55a60-281">`[TriggerPrivateBytesInKb <Int32?>]`: Özel baytları temel alan bir kural.</span><span class="sxs-lookup"><span data-stu-id="55a60-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="55a60-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Durum kodlarına dayalı bir kural.</span><span class="sxs-lookup"><span data-stu-id="55a60-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="55a60-283">`[Count <Int32?>]`: İstek sayısı.</span><span class="sxs-lookup"><span data-stu-id="55a60-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="55a60-284">`[Status <Int32?>]`: HTTP durum kodu.</span><span class="sxs-lookup"><span data-stu-id="55a60-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="55a60-285">`[SubStatus <Int32?>]`: Sub durumu talep edin.</span><span class="sxs-lookup"><span data-stu-id="55a60-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="55a60-286">`[TimeInterval <String>]`: Zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="55a60-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="55a60-287">`[Win32Status <Int32?>]`: Win32 hata kodu.</span><span class="sxs-lookup"><span data-stu-id="55a60-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="55a60-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bit çalışan işlemini kullanmak için; Aksi halde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-289">`[VirtualApplication <IVirtualApplication[]>]`: Sanal uygulamalar.</span><span class="sxs-lookup"><span data-stu-id="55a60-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="55a60-290">`[PhysicalPath <String>]`: Fiziksel yol.</span><span class="sxs-lookup"><span data-stu-id="55a60-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="55a60-291">`[PreloadEnabled <Boolean?>]`: önceden <code>true</code> önyüklemesi etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="55a60-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Sanal uygulama için sanal dizinler.</span><span class="sxs-lookup"><span data-stu-id="55a60-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="55a60-293">`[PhysicalPath <String>]`: Fiziksel yol.</span><span class="sxs-lookup"><span data-stu-id="55a60-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="55a60-294">`[VirtualPath <String>]`: Sanal uygulamanın yolu.</span><span class="sxs-lookup"><span data-stu-id="55a60-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="55a60-295">`[VirtualPath <String>]`: Sanal yol.</span><span class="sxs-lookup"><span data-stu-id="55a60-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="55a60-296">`[VnetName <String>]`: Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="55a60-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="55a60-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="55a60-298">`[WindowsFxVersion <String>]`: Xenon App Framework ve sürümü</span><span class="sxs-lookup"><span data-stu-id="55a60-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="55a60-299">`[XManagedServiceIdentityId <Int32?>]`: Açık yönetilen hizmet kimliği kimliği</span><span class="sxs-lookup"><span data-stu-id="55a60-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="55a60-300">`[ContainerSize <Int32?>]`: İşlev kapsayıcısının boyutu.</span><span class="sxs-lookup"><span data-stu-id="55a60-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="55a60-301">`[DailyMemoryTimeQuota <Int32?>]`: İzin verilen maksimum günlük bellek süresi kotası (yalnızca dinamik uygulamalarda uygulanabilir).</span><span class="sxs-lookup"><span data-stu-id="55a60-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="55a60-302">`[Enabled <Boolean?>]`: <code>true</code> uygulama etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="55a60-303">Bu değeri false olarak ayarlamak uygulamayı devre dışı bırakır (uygulamayı çevrimdışı duruma getirin).</span><span class="sxs-lookup"><span data-stu-id="55a60-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="55a60-304">`[HostNameSslState <IHostNameSslState[]>]`: Ana bilgisayar adı SSL durumları, uygulamanın ana bilgisayar adlarının SSL bağlarını yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="55a60-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="55a60-305">`[HostType <HostType?>]`: Ana bilgisayar adının standart mı yoksa havuz ana bilgisayar adı mı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a60-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="55a60-306">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="55a60-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="55a60-307">`[SslState <SslState?>]`: SSL türü.</span><span class="sxs-lookup"><span data-stu-id="55a60-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="55a60-308">`[Thumbprint <String>]`: SSL sertifikası parmak izi.</span><span class="sxs-lookup"><span data-stu-id="55a60-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="55a60-309">`[ToUpdate <Boolean?>]`: <code>true</code> Var olan konak adını güncelleştirecek şekilde ayarla.</span><span class="sxs-lookup"><span data-stu-id="55a60-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="55a60-310">`[VirtualIP <String>]`: IP tabanlı SSL etkinleştirilmişse ana bilgisayar adına atanan sanal IP adresi.</span><span class="sxs-lookup"><span data-stu-id="55a60-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="55a60-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> uygulamanın genel ana bilgisayar adlarını devre dışı bırakmak için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="55a60-312">Bu <code>true</code> uygulamaya yalnızca API yönetim işlemi aracılığıyla erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="55a60-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="55a60-313">`[HostingEnvironmentProfileId <String>]`: App Service ortamının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="55a60-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="55a60-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: yalnızca https isteklerini kabul edecek bir Web sitesi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="55a60-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="55a60-315">Http isteklerini yeniden yönlendirme sorunları</span><span class="sxs-lookup"><span data-stu-id="55a60-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="55a60-316">`[HyperV <Boolean?>]`: Hyper-V korumalı alanı.</span><span class="sxs-lookup"><span data-stu-id="55a60-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="55a60-317">`[IdentityType <ManagedServiceIdentityType?>]`: Yönetilen hizmet kimliğinin türü.</span><span class="sxs-lookup"><span data-stu-id="55a60-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="55a60-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Kaynakla ilişkili kullanıcı kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="55a60-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="55a60-319">Kullanıcı kimliği sözlüğü anahtar başvurularının formda ARM kaynak kimlikleri olur: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="55a60-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="55a60-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55a60-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="55a60-321">`[IsXenon <Boolean?>]`: Geçersiz: Hyper-V korumalı alanı.</span><span class="sxs-lookup"><span data-stu-id="55a60-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="55a60-322">`[RedundancyMode <RedundancyMode?>]`: Site artıklık modu</span><span class="sxs-lookup"><span data-stu-id="55a60-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="55a60-323">`[Reserved <Boolean?>]`: <code>true</code> tahsis edilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="55a60-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> uygulama DURDURULDUĞUNDA SCM (KUDU) sitesini durdurmak için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="55a60-325">Varsayılan değer <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="55a60-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="55a60-326">`[ServerFarmId <String>]`: İlişkili App Service planının kaynak KIMLIĞI,: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}" olarak biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="55a60-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="55a60-327">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55a60-327">RELATED LINKS</span></span>

