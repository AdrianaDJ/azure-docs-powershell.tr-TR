---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275407"
---
# <span data-ttu-id="83880-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="83880-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="83880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83880-102">SYNOPSIS</span></span>
<span data-ttu-id="83880-103">İşlev uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="83880-103">Updates a function app.</span></span>

## <span data-ttu-id="83880-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83880-104">SYNTAX</span></span>

### <span data-ttu-id="83880-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83880-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83880-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="83880-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="83880-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="83880-107">DESCRIPTION</span></span>
<span data-ttu-id="83880-108">İşlev uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="83880-108">Updates a function app.</span></span>

## <span data-ttu-id="83880-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83880-109">EXAMPLES</span></span>

### <span data-ttu-id="83880-110">Örnek 1: güncelleştirme işlevi uygulama barındırma planı.</span><span class="sxs-lookup"><span data-stu-id="83880-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="83880-111">Bu komut işlev uygulaması barındırma planını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="83880-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="83880-112">Örnek 2: işlev uygulaması için SystemAssigned yönetilen kimliği ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83880-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="83880-113">Bu komut, bir işlev uygulaması için SystemAssigned yönetilen kimliğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83880-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="83880-114">Örnek 3: güncelleştirme işlevi uygulama uygulaması öngörüleri.</span><span class="sxs-lookup"><span data-stu-id="83880-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="83880-115">Bu komut, App Application Insights işlevini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="83880-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="83880-116">Örnek 3: bir işlev uygulamasından yönetilen kimliği kaldırın.</span><span class="sxs-lookup"><span data-stu-id="83880-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="83880-117">Bu komut bir işlev uygulamasından yönetilen kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83880-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="83880-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83880-118">PARAMETERS</span></span>

### <span data-ttu-id="83880-119">-Applicationınsightskey</span><span class="sxs-lookup"><span data-stu-id="83880-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="83880-120">Application Insights 'ın alt yapısı</span><span class="sxs-lookup"><span data-stu-id="83880-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83880-121">-Applicationınsightsname</span><span class="sxs-lookup"><span data-stu-id="83880-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="83880-122">İşlev uygulamasına eklenecek mevcut App Insights projesinin adı.</span><span class="sxs-lookup"><span data-stu-id="83880-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83880-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="83880-123">-AsJob</span></span>
<span data-ttu-id="83880-124">Cmdlet 'i arka plan işi olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="83880-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="83880-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83880-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="83880-126">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="83880-126">-IdentityID</span></span>
<span data-ttu-id="83880-127">İşlev uygulamasıyla ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83880-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="83880-128">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="83880-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83880-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="83880-129">-IdentityType</span></span>
<span data-ttu-id="83880-130">İşlev uygulaması için kullanılan kimliğin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="83880-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="83880-131">' None ' türü işlev uygulamasından tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83880-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="83880-132">Bu parametre için kabul edilebilir değerler şunlardır:-SystemAssigned-Useratandı-yok</span><span class="sxs-lookup"><span data-stu-id="83880-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83880-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83880-133">-InputObject</span></span>
<span data-ttu-id="83880-134">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="83880-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83880-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="83880-135">-Name</span></span>
<span data-ttu-id="83880-136">İşlev uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="83880-136">The name of the function app.</span></span>

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

### <span data-ttu-id="83880-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="83880-137">-NoWait</span></span>
<span data-ttu-id="83880-138">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="83880-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="83880-139">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="83880-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="83880-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="83880-140">-PlanName</span></span>
<span data-ttu-id="83880-141">Hizmet planının adı.</span><span class="sxs-lookup"><span data-stu-id="83880-141">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83880-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83880-142">-ResourceGroupName</span></span>
<span data-ttu-id="83880-143">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="83880-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="83880-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="83880-144">-SubscriptionId</span></span>
<span data-ttu-id="83880-145">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83880-145">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="83880-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="83880-146">-Tag</span></span>
<span data-ttu-id="83880-147">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="83880-147">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83880-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="83880-148">-Confirm</span></span>
<span data-ttu-id="83880-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83880-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83880-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83880-150">-WhatIf</span></span>
<span data-ttu-id="83880-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83880-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83880-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83880-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83880-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83880-153">CommonParameters</span></span>
<span data-ttu-id="83880-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83880-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83880-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83880-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83880-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83880-156">INPUTS</span></span>

### <span data-ttu-id="83880-157">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="83880-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="83880-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83880-158">OUTPUTS</span></span>

### <span data-ttu-id="83880-159">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="83880-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="83880-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83880-160">NOTES</span></span>

<span data-ttu-id="83880-161">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="83880-161">ALIASES</span></span>

<span data-ttu-id="83880-162">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="83880-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83880-163">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="83880-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83880-164">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83880-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83880-165">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="83880-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="83880-166">`Location <String>`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="83880-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="83880-167">`CloningInfoSourceWebAppId <String>`: Kaynak uygulamanın ARM kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83880-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="83880-168">Uygulama kaynak KIMLIĞI, diğer yuvalarda üretim yuvaları ve/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} için/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} form.</span><span class="sxs-lookup"><span data-stu-id="83880-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="83880-169">`[Kind <String>]`: Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="83880-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="83880-170">`[Tag <IResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="83880-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="83880-171">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="83880-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="83880-172">`[ClientAffinityEnabled <Boolean?>]`: istemci <code>true</code> benzeşimini etkinleştirmek için; <code>false</code> istemci isteklerini aynı aynı aynı oturumda yönlendiren oturum benzeşimi tanımlama bilgilerini göndermeyi durdurmak için.</span><span class="sxs-lookup"><span data-stu-id="83880-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="83880-173">Varsayılan <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="83880-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> istemci sertifikası kimlik doğrulamasını etkinleştirmek için (TLS karşılıklı kimlik doğrulaması); Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="83880-175">Varsayılan <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="83880-176">`[ClientCertExclusionPath <String>]`: istemci sertifikası kimlik doğrulaması virgülle ayrılmış dışlama yolları</span><span class="sxs-lookup"><span data-stu-id="83880-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="83880-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Kopyalanan uygulama için uygulama ayarı geçersiz kılmaları.</span><span class="sxs-lookup"><span data-stu-id="83880-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="83880-178">Belirtilmişse, bu ayarlar kaynak uygulamadan kopyalanan ayarları geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="83880-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="83880-179">Aksi takdirde, kaynak uygulamadaki uygulama ayarları korunur.</span><span class="sxs-lookup"><span data-stu-id="83880-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="83880-180">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="83880-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="83880-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> kaynak uygulamadan özel konak adları kopyalamak için; Aksi halde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="83880-182">`[CloningInfoCloneSourceControl <Boolean?>]`: kaynak <code>true</code> uygulamayı kaynak uygulamadan kopyalamak için; Aksi halde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="83880-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> kaynak ve hedef uygulama için yük dengelemeyi yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="83880-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="83880-184">`[CloningInfoCorrelationId <String>]`: Kopyalama işleminin bağıntı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83880-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="83880-185">Bu KIMLIK birden çok klonlama işlemini aynı anlık görüntüyü kullanacak şekilde bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="83880-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="83880-186">`[CloningInfoHostingEnvironment <String>]`: App Service ortamı.</span><span class="sxs-lookup"><span data-stu-id="83880-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="83880-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> hedef uygulamanın üzerine yazmak için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="83880-188">`[CloningInfoSourceWebAppLocation <String>]`: Kaynak uygulama EX 'ın konumu: Batı ABD veya Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="83880-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="83880-189">`[CloningInfoTrafficManagerProfileId <String>]`: Varsa, kullanılacak Traffic Manager profilinin kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83880-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="83880-190">Traffic Manager kaynak KIMLIĞI/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="83880-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="83880-191">`[CloningInfoTrafficManagerProfileName <String>]`: Oluşturulacak Traffic Manager profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="83880-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="83880-192">Bu yalnızca Traffic Manager profili yoksa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="83880-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="83880-193">`[Config <ISiteConfig>]`: Uygulamanın yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="83880-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="83880-194">`IsPushEnabled <Boolean>`: Itme uç noktasının etkinleştirilip etkinleştirilmediğini belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83880-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="83880-195">`[ActionMinProcessExecutionTime <String>]`: İşlemin önüne geçmeden önce işlemin yürütülmesi gereken minimum süre</span><span class="sxs-lookup"><span data-stu-id="83880-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="83880-196">`[ActionType <AutoHealActionType?>]`: Önceden tanımlanmış eylem gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="83880-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="83880-197">`[AlwaysOn <Boolean?>]`: <code>true</code> her zaman açık etkinleştirilirse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-198">`[ApiDefinitionUrl <String>]`: API tanımının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="83880-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="83880-199">`[ApiManagementConfigId <String>]`: APIM-Api tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="83880-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="83880-200">`[AppCommandLine <String>]`: Başlatılacak uygulama komut satırı.</span><span class="sxs-lookup"><span data-stu-id="83880-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="83880-201">`[AppSetting <INameValuePair[]>]`: Uygulama ayarları.</span><span class="sxs-lookup"><span data-stu-id="83880-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="83880-202">`[Name <String>]`: Çift adı.</span><span class="sxs-lookup"><span data-stu-id="83880-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="83880-203">`[Value <String>]`: Çift değer.</span><span class="sxs-lookup"><span data-stu-id="83880-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="83880-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Otomatik Heal etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-205">`[AutoSwapSlotName <String>]`: Yuva adı otomatik takas et.</span><span class="sxs-lookup"><span data-stu-id="83880-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="83880-206">`[ConnectionString <IConnStringInfo[]>]`: Bağlantı dizeleri.</span><span class="sxs-lookup"><span data-stu-id="83880-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="83880-207">`[ConnectionString <String>]`: Bağlantı dizesi değeri.</span><span class="sxs-lookup"><span data-stu-id="83880-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="83880-208">`[Name <String>]`: Bağlantı dizesinin adı.</span><span class="sxs-lookup"><span data-stu-id="83880-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="83880-209">`[Type <ConnectionStringType?>]`: Veritabanı türü.</span><span class="sxs-lookup"><span data-stu-id="83880-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="83880-210">`[CorAllowedOrigin <String[]>]`: Çapraz kaynak çağrıları yapmasına izin verilmesi gereken kaynak listesini alır veya ayarlar (örneğin: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="83880-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="83880-211">Tümüne izin vermek için "\*" kullanın.</span><span class="sxs-lookup"><span data-stu-id="83880-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="83880-212">`[CorSupportCredentials <Boolean?>]`: Kimlik bilgilerinin bulunduğu CORS isteklerine izin verilip verilmediğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83880-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="83880-213"> https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentialsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="83880-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="83880-214">`[CustomActionExe <String>]`: Çalıştırılabilir dosya.</span><span class="sxs-lookup"><span data-stu-id="83880-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="83880-215">`[CustomActionParameter <String>]`: Çalıştırılabilirin parametreleri.</span><span class="sxs-lookup"><span data-stu-id="83880-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="83880-216">`[DefaultDocument <String[]>]`: Varsayılan belgeler.</span><span class="sxs-lookup"><span data-stu-id="83880-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="83880-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> ayrıntılı hata günlüğü etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-218">`[DocumentRoot <String>]`: Belge kökü.</span><span class="sxs-lookup"><span data-stu-id="83880-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="83880-219">`[DynamicTagsJson <String>]`: İtme kaydı uç noktasındaki Kullanıcı taleplerini değerlendirilecek dinamik etiket listesini içeren bir JSON dizesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83880-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="83880-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: Rampa kuralları listesi.</span><span class="sxs-lookup"><span data-stu-id="83880-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="83880-221">`[ActionHostName <String>]`: Karar verirse trafiğin yönlendirileceği bir yuvanın ana bilgisayarı.</span><span class="sxs-lookup"><span data-stu-id="83880-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="83880-222">Yani.</span><span class="sxs-lookup"><span data-stu-id="83880-222">E.g.</span></span> <span data-ttu-id="83880-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="83880-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="83880-224">`[ChangeDecisionCallbackUrl <String>]`: Özel karar algoritması, TiPCallback site uzantısında hangi URL belirtibileceğine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="83880-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="83880-225">Scaffold ve sözleşmeler için TiPCallback site uzantısına bakın.</span><span class="sxs-lookup"><span data-stu-id="83880-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="83880-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="83880-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="83880-227">`[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="83880-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="83880-228">`[ChangeStep <Double?>]`: Otomatik artırma senaryosunda, bu, <code>ReroutePercentage</code> \n <code>MinReroutePercentage</code> veya         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="83880-229">Site ölçümleri, her N dakikada bir işaretlenmelidir <code>ChangeIntervalInMinutes</code> . \nözel karar algoritması, Ýpucu <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="83880-230">`[MaxReroutePercentage <Double?>]`: ReroutePercentage 'in hangi üst sınıra kalacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83880-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="83880-231">`[MinReroutePercentage <Double?>]`: ReroutePercentage 'in üzerinde kalacağı alt sınırı belirtir.</span><span class="sxs-lookup"><span data-stu-id="83880-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="83880-232">`[Name <String>]`: Yönlendirme kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="83880-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="83880-233">Önerilen ad, denemeler sırasında trafiği alacak olan yuvanın üzerine gelmek olacaktır.</span><span class="sxs-lookup"><span data-stu-id="83880-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="83880-234">`[ReroutePercentage <Double?>]`: Yönlendirileceği trafiğin yüzdesi <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="83880-235">`[FtpsState <FtpsState?>]`: FTP/FTPS hizmetinin durumu</span><span class="sxs-lookup"><span data-stu-id="83880-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="83880-236">`[HandlerMapping <IHandlerMapping[]>]`: İşleyici eşlemeleri.</span><span class="sxs-lookup"><span data-stu-id="83880-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="83880-237">`[Argument <String>]`: Betik işlemcisine geçirilecek komut satırı bağımsız değişkenleri.</span><span class="sxs-lookup"><span data-stu-id="83880-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="83880-238">`[Extension <String>]`: Bu uzantıya sahip istekler belirtilen FastCGI uygulaması kullanılarak işlenecek.</span><span class="sxs-lookup"><span data-stu-id="83880-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="83880-239">`[ScriptProcessor <String>]`: FastCGI uygulamasının mutlak yolu.</span><span class="sxs-lookup"><span data-stu-id="83880-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="83880-240">`[HealthCheckPath <String>]`: Sağlık denetleme yolu</span><span class="sxs-lookup"><span data-stu-id="83880-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="83880-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: istemcilerin http 2.0 üzerinden bağlanmasına olanak tanımak için bir Web sitesi yapılandırır</span><span class="sxs-lookup"><span data-stu-id="83880-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="83880-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> http günlüğü etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Main için IP güvenlik kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="83880-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="83880-244">`[Action <String>]`: Bu IP aralığına erişim izni verin veya erişimi reddedin.</span><span class="sxs-lookup"><span data-stu-id="83880-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="83880-245">`[Description <String>]`: IP kısıtlama kuralı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="83880-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="83880-246">`[IPAddress <String>]`: IP adresi güvenlik kısıtlamasının geçerlilik olduğu.</span><span class="sxs-lookup"><span data-stu-id="83880-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="83880-247">Saf IPv4 adresi (gerekli AltAğMaskesi özelliği) veya IPv4/maske (önde gelen bit eşleşmesi) gibi CıDR gösterimi biçiminde olabilir.</span><span class="sxs-lookup"><span data-stu-id="83880-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="83880-248">CıDR için AltAğMaskesi özelliği belirtilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="83880-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="83880-249">`[Name <String>]`: IP kısıtlama kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="83880-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="83880-250">`[Priority <Int32?>]`: IP kısıtlama kuralının önceliği.</span><span class="sxs-lookup"><span data-stu-id="83880-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="83880-251">`[SubnetMask <String>]`: Kısıtlamanın geçerli olduğu IP adresi aralığı için alt ağ maskesi.</span><span class="sxs-lookup"><span data-stu-id="83880-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="83880-252">`[SubnetTrafficTag <Int32?>]`: (iç) alt ağ trafiği etiketi</span><span class="sxs-lookup"><span data-stu-id="83880-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="83880-253">`[Tag <IPFilterTag?>]`: Bu IP Filtresinin hangi şekilde kullanılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="83880-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="83880-254">Bu, proxy 'lerde IP filtrelemesinin desteklenmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83880-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="83880-255">`[VnetSubnetResourceId <String>]`: Sanal ağ kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="83880-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="83880-256">`[VnetTrafficTag <Int32?>]`: (iç) VNET trafiği etiketi</span><span class="sxs-lookup"><span data-stu-id="83880-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="83880-257">`[JavaContainer <String>]`: Java kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="83880-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="83880-258">`[JavaContainerVersion <String>]`: Java kapsayıcı sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="83880-259">`[JavaVersion <String>]`: Java sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="83880-260">`[LimitMaxDiskSizeInMb <Int64?>]`: İzin verilen maksimum MB cinsinden disk boyutu kullanımı.</span><span class="sxs-lookup"><span data-stu-id="83880-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="83880-261">`[LimitMaxMemoryInMb <Int64?>]`: MB cinsinden izin verilen en fazla bellek kullanımı.</span><span class="sxs-lookup"><span data-stu-id="83880-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="83880-262">`[LimitMaxPercentageCpu <Double?>]`: İzin verilen en yüksek CPU kullanımı yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="83880-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="83880-263">`[LinuxFxVersion <String>]`: Linux uygulama çerçevesi ve sürümü</span><span class="sxs-lookup"><span data-stu-id="83880-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="83880-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site yük dengelemesi.</span><span class="sxs-lookup"><span data-stu-id="83880-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="83880-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> Yerel MySQL 'yı etkinleştirmek için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP günlükleri Dizin boyutu sınırını aşıyor.</span><span class="sxs-lookup"><span data-stu-id="83880-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="83880-267">`[MachineKeyDecryption <String>]`: Şifre çözme için kullanılan algoritma.</span><span class="sxs-lookup"><span data-stu-id="83880-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="83880-268">`[MachineKeyDecryptionKey <String>]`: Şifre çözme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="83880-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="83880-269">`[MachineKeyValidation <String>]`: MachineKey doğrulama.</span><span class="sxs-lookup"><span data-stu-id="83880-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="83880-270">`[MachineKeyValidationKey <String>]`: Geçerlilik anahtarı.</span><span class="sxs-lookup"><span data-stu-id="83880-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="83880-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Yönetilen ardışık düzen modu.</span><span class="sxs-lookup"><span data-stu-id="83880-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="83880-272">`[ManagedServiceIdentityId <Int32?>]`: Yönetilen hizmet kimliği kimliği</span><span class="sxs-lookup"><span data-stu-id="83880-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="83880-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL istekleri için gereken en düşük TLS sürümünü yapılandırır</span><span class="sxs-lookup"><span data-stu-id="83880-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="83880-274">`[NetFrameworkVersion <String>]`: .NET Framework sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="83880-275">`[NodeVersion <String>]`: Node.js sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="83880-276">`[NumberOfWorker <Int32?>]`: Çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="83880-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="83880-277">`[PhpVersion <String>]`: PHP sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="83880-278">`[PowerShellVersion <String>]`: PowerShell sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="83880-279">`[PreWarmedInstanceCount <Int32?>]`: Ön ödeme örneklerinin sayısı.</span><span class="sxs-lookup"><span data-stu-id="83880-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="83880-280">Bu ayar yalnızca tüketim ve esnek planlar için geçerlidir</span><span class="sxs-lookup"><span data-stu-id="83880-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="83880-281">`[PublishingUsername <String>]`: Kullanıcı adı yayımlanıyor.</span><span class="sxs-lookup"><span data-stu-id="83880-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="83880-282">`[PushKind <String>]`: Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="83880-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="83880-283">`[PythonVersion <String>]`: Python sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="83880-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Uzaktan hata ayıklama etkinse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-285">`[RemoteDebuggingVersion <String>]`: Uzaktan hata ayıklama sürümü.</span><span class="sxs-lookup"><span data-stu-id="83880-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="83880-286">`[RequestCount <Int32?>]`: İstek sayısı.</span><span class="sxs-lookup"><span data-stu-id="83880-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="83880-287">`[RequestTimeInterval <String>]`: Zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="83880-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="83880-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> istek izleme etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-289">`[RequestTracingExpirationTime <DateTime?>]`: İstek izleme süre sonu.</span><span class="sxs-lookup"><span data-stu-id="83880-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="83880-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: SCM için IP güvenlik kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="83880-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="83880-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: SCM 'nin Main kullanması için IP güvenlik kısıtlamaları.</span><span class="sxs-lookup"><span data-stu-id="83880-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="83880-292">`[ScmType <ScmType?>]`: SCM türü.</span><span class="sxs-lookup"><span data-stu-id="83880-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="83880-293">`[SlowRequestCount <Int32?>]`: İstek sayısı.</span><span class="sxs-lookup"><span data-stu-id="83880-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="83880-294">`[SlowRequestTimeInterval <String>]`: Zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="83880-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="83880-295">`[SlowRequestTimeTaken <String>]`: Geçen süre.</span><span class="sxs-lookup"><span data-stu-id="83880-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="83880-296">`[TagWhitelistJson <String>]`: İtme kaydı uç noktası tarafından kullanılmak üzere, beyaz listelenen etiket listesini içeren bir JSON dizesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83880-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="83880-297">`[TagsRequiringAuth <String>]`: İtme kaydı uç noktasında kullanılacak kullanıcı kimlik doğrulaması gerektiren etiket listesini içeren bir JSON dizesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83880-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="83880-298">Etiketler alfasayısal karakterler ve aşağıdakiler: ' _ ', ' @ ', ' # ', '. ', ': ', '-'.</span><span class="sxs-lookup"><span data-stu-id="83880-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="83880-299">Doğrulama, PushRequestHandler ' de gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="83880-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="83880-300">`[TracingOption <String>]`: İzleme seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="83880-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="83880-301">`[TriggerPrivateBytesInKb <Int32?>]`: Özel baytları temel alan bir kural.</span><span class="sxs-lookup"><span data-stu-id="83880-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="83880-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Durum kodlarına dayalı bir kural.</span><span class="sxs-lookup"><span data-stu-id="83880-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="83880-303">`[Count <Int32?>]`: İstek sayısı.</span><span class="sxs-lookup"><span data-stu-id="83880-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="83880-304">`[Status <Int32?>]`: HTTP durum kodu.</span><span class="sxs-lookup"><span data-stu-id="83880-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="83880-305">`[SubStatus <Int32?>]`: Sub durumu talep edin.</span><span class="sxs-lookup"><span data-stu-id="83880-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="83880-306">`[TimeInterval <String>]`: Zaman aralığı.</span><span class="sxs-lookup"><span data-stu-id="83880-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="83880-307">`[Win32Status <Int32?>]`: Win32 hata kodu.</span><span class="sxs-lookup"><span data-stu-id="83880-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="83880-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 bit çalışan işlemini kullanmak için; Aksi halde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-309">`[VirtualApplication <IVirtualApplication[]>]`: Sanal uygulamalar.</span><span class="sxs-lookup"><span data-stu-id="83880-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="83880-310">`[PhysicalPath <String>]`: Fiziksel yol.</span><span class="sxs-lookup"><span data-stu-id="83880-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="83880-311">`[PreloadEnabled <Boolean?>]`: önceden <code>true</code> önyüklemesi etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="83880-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Sanal uygulama için sanal dizinler.</span><span class="sxs-lookup"><span data-stu-id="83880-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="83880-313">`[PhysicalPath <String>]`: Fiziksel yol.</span><span class="sxs-lookup"><span data-stu-id="83880-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="83880-314">`[VirtualPath <String>]`: Sanal uygulamanın yolu.</span><span class="sxs-lookup"><span data-stu-id="83880-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="83880-315">`[VirtualPath <String>]`: Sanal yol.</span><span class="sxs-lookup"><span data-stu-id="83880-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="83880-316">`[VnetName <String>]`: Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="83880-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="83880-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="83880-318">`[WindowsFxVersion <String>]`: Xenon App Framework ve sürümü</span><span class="sxs-lookup"><span data-stu-id="83880-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="83880-319">`[XManagedServiceIdentityId <Int32?>]`: Açık yönetilen hizmet kimliği kimliği</span><span class="sxs-lookup"><span data-stu-id="83880-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="83880-320">`[ContainerSize <Int32?>]`: İşlev kapsayıcısının boyutu.</span><span class="sxs-lookup"><span data-stu-id="83880-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="83880-321">`[DailyMemoryTimeQuota <Int32?>]`: İzin verilen maksimum günlük bellek süresi kotası (yalnızca dinamik uygulamalarda uygulanabilir).</span><span class="sxs-lookup"><span data-stu-id="83880-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="83880-322">`[Enabled <Boolean?>]`: <code>true</code> uygulama etkinleştirilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="83880-323">Bu değeri false olarak ayarlamak uygulamayı devre dışı bırakır (uygulamayı çevrimdışı duruma getirin).</span><span class="sxs-lookup"><span data-stu-id="83880-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="83880-324">`[HostNameSslState <IHostNameSslState[]>]`: Ana bilgisayar adı SSL durumları, uygulamanın ana bilgisayar adlarının SSL bağlarını yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83880-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="83880-325">`[HostType <HostType?>]`: Ana bilgisayar adının standart mı yoksa havuz ana bilgisayar adı mı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="83880-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="83880-326">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="83880-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="83880-327">`[SslState <SslState?>]`: SSL türü.</span><span class="sxs-lookup"><span data-stu-id="83880-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="83880-328">`[Thumbprint <String>]`: SSL sertifikası parmak izi.</span><span class="sxs-lookup"><span data-stu-id="83880-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="83880-329">`[ToUpdate <Boolean?>]`: <code>true</code> Var olan konak adını güncelleştirecek şekilde ayarla.</span><span class="sxs-lookup"><span data-stu-id="83880-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="83880-330">`[VirtualIP <String>]`: IP tabanlı SSL etkinleştirilmişse ana bilgisayar adına atanan sanal IP adresi.</span><span class="sxs-lookup"><span data-stu-id="83880-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="83880-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> uygulamanın genel ana bilgisayar adlarını devre dışı bırakmak için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="83880-332">Bu <code>true</code> uygulamaya yalnızca API yönetim işlemi aracılığıyla erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="83880-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="83880-333">`[HostingEnvironmentProfileId <String>]`: App Service ortamının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="83880-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="83880-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: yalnızca https isteklerini kabul edecek bir Web sitesi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="83880-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="83880-335">Http isteklerini yeniden yönlendirme sorunları</span><span class="sxs-lookup"><span data-stu-id="83880-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="83880-336">`[HyperV <Boolean?>]`: Hyper-V korumalı alanı.</span><span class="sxs-lookup"><span data-stu-id="83880-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="83880-337">`[IdentityType <ManagedServiceIdentityType?>]`: Yönetilen hizmet kimliğinin türü.</span><span class="sxs-lookup"><span data-stu-id="83880-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="83880-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Kaynakla ilişkili kullanıcı kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="83880-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="83880-339">Kullanıcı kimliği sözlüğü anahtar başvurularının formda ARM kaynak kimlikleri olur: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="83880-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="83880-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="83880-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="83880-341">`[IsXenon <Boolean?>]`: Geçersiz: Hyper-V korumalı alanı.</span><span class="sxs-lookup"><span data-stu-id="83880-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="83880-342">`[RedundancyMode <RedundancyMode?>]`: Site artıklık modu</span><span class="sxs-lookup"><span data-stu-id="83880-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="83880-343">`[Reserved <Boolean?>]`: <code>true</code> tahsis edilmişse; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="83880-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> uygulama DURDURULDUĞUNDA SCM (KUDU) sitesini durdurmak için; Aksi takdirde <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="83880-345">Varsayılan değer <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="83880-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="83880-346">`[ServerFarmId <String>]`: İlişkili App Service planının kaynak KIMLIĞI,: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}" olarak biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="83880-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="83880-347">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83880-347">RELATED LINKS</span></span>

