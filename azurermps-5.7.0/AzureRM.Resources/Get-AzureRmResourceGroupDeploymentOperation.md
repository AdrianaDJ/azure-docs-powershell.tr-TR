---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588801"
---
# <span data-ttu-id="00554-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="00554-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="00554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00554-102">SYNOPSIS</span></span>
<span data-ttu-id="00554-103">Kaynak grubu dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="00554-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00554-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00554-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="00554-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00554-105">DESCRIPTION</span></span>
<span data-ttu-id="00554-106">**Get-AzureRmResourceGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="00554-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="00554-107">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="00554-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="00554-108">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="00554-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="00554-109">İsteği ve yanıt içeriğini almak için, **Yeni-AzureRmResourceGroupDeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="00554-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="00554-110">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="00554-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="00554-111">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="00554-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="00554-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00554-112">EXAMPLES</span></span>

### <span data-ttu-id="00554-113">Get1</span><span class="sxs-lookup"><span data-stu-id="00554-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="00554-114">"Test" kaynak grubu altındaki "test" adlı dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="00554-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="00554-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00554-115">PARAMETERS</span></span>

### <span data-ttu-id="00554-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="00554-116">-ApiVersion</span></span>
<span data-ttu-id="00554-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="00554-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="00554-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="00554-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00554-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00554-119">-DefaultProfile</span></span>
<span data-ttu-id="00554-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="00554-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00554-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="00554-121">-DeploymentName</span></span>
<span data-ttu-id="00554-122">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="00554-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00554-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="00554-123">-InformationAction</span></span>
<span data-ttu-id="00554-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00554-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="00554-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="00554-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00554-126">'A</span><span class="sxs-lookup"><span data-stu-id="00554-126">Continue</span></span>
- <span data-ttu-id="00554-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="00554-127">Ignore</span></span>
- <span data-ttu-id="00554-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="00554-128">Inquire</span></span>
- <span data-ttu-id="00554-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="00554-129">SilentlyContinue</span></span>
- <span data-ttu-id="00554-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="00554-130">Stop</span></span>
- <span data-ttu-id="00554-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="00554-131">Suspend</span></span>

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

### <span data-ttu-id="00554-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="00554-132">-InformationVariable</span></span>
<span data-ttu-id="00554-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="00554-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="00554-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="00554-134">-Pre</span></span>
<span data-ttu-id="00554-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00554-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="00554-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00554-136">-ResourceGroupName</span></span>
<span data-ttu-id="00554-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="00554-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00554-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="00554-138">-SubscriptionId</span></span>
<span data-ttu-id="00554-139">Kullanılacak abonelik.</span><span class="sxs-lookup"><span data-stu-id="00554-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00554-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00554-140">CommonParameters</span></span>
<span data-ttu-id="00554-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00554-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00554-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00554-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00554-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00554-143">INPUTS</span></span>

### <span data-ttu-id="00554-144">'Sine</span><span class="sxs-lookup"><span data-stu-id="00554-144">Guid</span></span>
<span data-ttu-id="00554-145">' SubscriptionID ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="00554-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="00554-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00554-146">OUTPUTS</span></span>

### <span data-ttu-id="00554-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="00554-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="00554-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00554-148">NOTES</span></span>

## <span data-ttu-id="00554-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00554-149">RELATED LINKS</span></span>
