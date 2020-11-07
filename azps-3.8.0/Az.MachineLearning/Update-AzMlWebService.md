---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a170d21a2301541f1346905ed701d477ecba4204
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937836"
---
# <span data-ttu-id="d84ff-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="d84ff-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="d84ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84ff-102">SYNOPSIS</span></span>
<span data-ttu-id="d84ff-103">Var olan bir Web hizmeti kaynağının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="d84ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d84ff-104">SYNTAX</span></span>

### <span data-ttu-id="d84ff-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="d84ff-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84ff-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="d84ff-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d84ff-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d84ff-107">DESCRIPTION</span></span>
<span data-ttu-id="d84ff-108">Update-AzMlWebService cmdlet 'i, Web servisinin statik olmayan özelliklerini güncelleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d84ff-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="d84ff-109">Cmdlet, düzeltme eki olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="d84ff-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="d84ff-110">Yalnızca değişiklik yapmak istediğiniz özellikleri geçirin.</span><span class="sxs-lookup"><span data-stu-id="d84ff-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="d84ff-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d84ff-111">EXAMPLES</span></span>

### <span data-ttu-id="d84ff-112">Örnek 1: seçmeli güncelleştirme bağımsız değişkenleri</span><span class="sxs-lookup"><span data-stu-id="d84ff-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="d84ff-113">Burada, Web hizmeti için çalışma zamanı sırasında açıklama, birincil erişim anahtarı değiştirilir ve tüm izlemeler için tanılama koleksiyonunu etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="d84ff-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="d84ff-114">Örnek 2: Web hizmeti örneğine dayalı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d84ff-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="d84ff-115">Örnek ilk olarak yalnızca güncelleştirilecek alanları içeren bir Web hizmeti tanımı oluşturur ve ardından, bu dosyaları ServiceUpdates parametresini kullanarak uygulamak için Update-AzMlWebService çağırır.</span><span class="sxs-lookup"><span data-stu-id="d84ff-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="d84ff-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d84ff-116">PARAMETERS</span></span>

### <span data-ttu-id="d84ff-117">-Kıymetler</span><span class="sxs-lookup"><span data-stu-id="d84ff-117">-Assets</span></span>
<span data-ttu-id="d84ff-118">Web hizmetini oluşturan varlık kümesi (örneğin modüller, veri kümeleri).</span><span class="sxs-lookup"><span data-stu-id="d84ff-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84ff-119">-DefaultProfile</span></span>
<span data-ttu-id="d84ff-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d84ff-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d84ff-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d84ff-121">-Description</span></span>
<span data-ttu-id="d84ff-122">Web hizmeti açıklamasına yönelik yeni değer.</span><span class="sxs-lookup"><span data-stu-id="d84ff-122">The new value for the web service's description.</span></span>
<span data-ttu-id="d84ff-123">Bu, hizmetin Swagger API şemasında görülebilir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-124">-Tanılama</span><span class="sxs-lookup"><span data-stu-id="d84ff-124">-Diagnostics</span></span>
<span data-ttu-id="d84ff-125">Web hizmeti için tanılama izlemeleri koleksiyonunu denetleyen ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d84ff-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d84ff-126">-Force</span></span>
<span data-ttu-id="d84ff-127">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="d84ff-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d84ff-128">-Giriş</span><span class="sxs-lookup"><span data-stu-id="d84ff-128">-Input</span></span>
<span data-ttu-id="d84ff-129">Swagger şema yapısı olarak sağlanan Web hizmeti girdisinin tanımı.</span><span class="sxs-lookup"><span data-stu-id="d84ff-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="d84ff-130">-IsReadOnly</span></span>
<span data-ttu-id="d84ff-131">Bu Web hizmetinin salt okunur olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="d84ff-132">Bir kez ayarlandıktan sonra, bu özelliğin değerini değiştirmek de içinde olmak üzere Web hizmeti artık güncelleştirilebilir ve yalnızca silinebilir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-133">Tuşları</span><span class="sxs-lookup"><span data-stu-id="d84ff-133">-Keys</span></span>
<span data-ttu-id="d84ff-134">Hizmetin çalışma zamanı API 'Lerine çağrı kimliklerinin doğrulanması için kullanılan erişim anahtarlarının birini veya her ikisini birden güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="d84ff-135">-Name</span></span>
<span data-ttu-id="d84ff-136">Güncelleştirilecek Web hizmeti kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d84ff-136">The name of the web service resource to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-137">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="d84ff-137">-Output</span></span>
<span data-ttu-id="d84ff-138">Swagger şema yapısı olarak sağlanan Web hizmeti çıkışının (s) tanımı.</span><span class="sxs-lookup"><span data-stu-id="d84ff-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-139">-Package</span><span class="sxs-lookup"><span data-stu-id="d84ff-139">-Package</span></span>
<span data-ttu-id="d84ff-140">Bu Web hizmetini tanımlayan grafik paketinin tanımı.</span><span class="sxs-lookup"><span data-stu-id="d84ff-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-141">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="d84ff-141">-Parameters</span></span>
<span data-ttu-id="d84ff-142">Web hizmeti için tanımlanmış, genel parametre adı olarak belirtilen genel parametre değerleri kümesi- \> varsayılan değer koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="d84ff-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="d84ff-143">Varsayılan bir değer belirtilmemişse, parametre gerekli kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d84ff-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="d84ff-145">Hizmetin gerçek uç noktası yapılandırmasına yönelik güncelleştirmeler.</span><span class="sxs-lookup"><span data-stu-id="d84ff-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84ff-146">-ResourceGroupName</span></span>
<span data-ttu-id="d84ff-147">Güncelleştirilecek Web servisini içeren kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d84ff-147">The resource group that contains the web service to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="d84ff-148">-ServiceUpdates</span></span>
<span data-ttu-id="d84ff-149">Web hizmeti tanımı örneği olarak sağlanan Web hizmetine uygulanacak güncelleştirmeler kümesi.</span><span class="sxs-lookup"><span data-stu-id="d84ff-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="d84ff-150">Yalnızca statik olmayan alanlar değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d84ff-151">-StorageAccountKey</span></span>
<span data-ttu-id="d84ff-152">Web hizmetiyle ilişkili depolama hesabının erişim tuşunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="d84ff-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-153">-Başlık</span><span class="sxs-lookup"><span data-stu-id="d84ff-153">-Title</span></span>
<span data-ttu-id="d84ff-154">Web hizmeti unvanı için yeni değer.</span><span class="sxs-lookup"><span data-stu-id="d84ff-154">The new value for the web service's title.</span></span>
<span data-ttu-id="d84ff-155">Bu, hizmetin Swagger API şemasında görülebilir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ff-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="d84ff-156">-Confirm</span></span>
<span data-ttu-id="d84ff-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d84ff-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84ff-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84ff-158">-WhatIf</span></span>
<span data-ttu-id="d84ff-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d84ff-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84ff-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d84ff-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d84ff-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84ff-161">CommonParameters</span></span>
<span data-ttu-id="d84ff-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d84ff-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84ff-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84ff-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84ff-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d84ff-164">INPUTS</span></span>

### <span data-ttu-id="d84ff-165">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="d84ff-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="d84ff-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d84ff-166">OUTPUTS</span></span>

### <span data-ttu-id="d84ff-167">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="d84ff-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="d84ff-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d84ff-168">NOTES</span></span>
<span data-ttu-id="d84ff-169">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d84ff-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d84ff-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d84ff-170">RELATED LINKS</span></span>
