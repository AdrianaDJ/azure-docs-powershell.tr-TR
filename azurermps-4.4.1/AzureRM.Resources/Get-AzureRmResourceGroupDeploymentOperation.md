---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: fd0ce106fe7d32b47afcb7962252407a74e163f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592577"
---
# <span data-ttu-id="d6190-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d6190-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="d6190-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6190-102">SYNOPSIS</span></span>
<span data-ttu-id="d6190-103">Kaynak grubu dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="d6190-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6190-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6190-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d6190-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6190-105">DESCRIPTION</span></span>
<span data-ttu-id="d6190-106">**Get-AzureRmResourceGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="d6190-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d6190-107">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="d6190-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="d6190-108">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="d6190-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="d6190-109">İsteği ve yanıt içeriğini almak için, **Yeni-AzureRmResourceGroupDeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="d6190-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="d6190-110">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="d6190-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="d6190-111">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d6190-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="d6190-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6190-112">EXAMPLES</span></span>

### <span data-ttu-id="d6190-113">--------------------------Get1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6190-113">--------------------------  Get1  --------------------------</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="d6190-114">"Test" kaynak grubu altındaki "test" adlı dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="d6190-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="d6190-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6190-115">PARAMETERS</span></span>

### <span data-ttu-id="d6190-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="d6190-116">-ApiVersion</span></span>
<span data-ttu-id="d6190-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6190-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6190-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d6190-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d6190-119">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d6190-119">-DeploymentName</span></span>
<span data-ttu-id="d6190-120">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="d6190-120">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6190-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d6190-121">-InformationAction</span></span>
<span data-ttu-id="d6190-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6190-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d6190-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d6190-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6190-124">'A</span><span class="sxs-lookup"><span data-stu-id="d6190-124">Continue</span></span>
- <span data-ttu-id="d6190-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="d6190-125">Ignore</span></span>
- <span data-ttu-id="d6190-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d6190-126">Inquire</span></span>
- <span data-ttu-id="d6190-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d6190-127">SilentlyContinue</span></span>
- <span data-ttu-id="d6190-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d6190-128">Stop</span></span>
- <span data-ttu-id="d6190-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d6190-129">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6190-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d6190-130">-InformationVariable</span></span>
<span data-ttu-id="d6190-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6190-131">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6190-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="d6190-132">-Pre</span></span>
<span data-ttu-id="d6190-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6190-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d6190-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6190-134">-ResourceGroupName</span></span>
<span data-ttu-id="d6190-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d6190-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6190-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d6190-136">-SubscriptionId</span></span>
<span data-ttu-id="d6190-137">Kullanılacak abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6190-137">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6190-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6190-138">-DefaultProfile</span></span>
<span data-ttu-id="d6190-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6190-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6190-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6190-140">CommonParameters</span></span>
<span data-ttu-id="d6190-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6190-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6190-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6190-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6190-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6190-143">INPUTS</span></span>

### <span data-ttu-id="d6190-144">'Sine</span><span class="sxs-lookup"><span data-stu-id="d6190-144">Guid</span></span>
<span data-ttu-id="d6190-145">' SubscriptionID ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d6190-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="d6190-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6190-146">OUTPUTS</span></span>

### <span data-ttu-id="d6190-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d6190-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d6190-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6190-148">NOTES</span></span>

## <span data-ttu-id="d6190-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6190-149">RELATED LINKS</span></span>

