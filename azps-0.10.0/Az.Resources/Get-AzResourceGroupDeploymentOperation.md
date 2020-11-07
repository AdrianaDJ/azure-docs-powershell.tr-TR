---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 22438110dd66fbbb89e992d79f37b1e8e2e325d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936425"
---
# <span data-ttu-id="2821f-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2821f-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="2821f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2821f-102">SYNOPSIS</span></span>
<span data-ttu-id="2821f-103">Kaynak grubu dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="2821f-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="2821f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2821f-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2821f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2821f-105">DESCRIPTION</span></span>
<span data-ttu-id="2821f-106">**Get-AzResourceGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="2821f-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="2821f-107">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="2821f-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="2821f-108">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="2821f-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="2821f-109">İsteği ve yanıt içeriğini almak için, **Yeni-AzResourceGroupDeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2821f-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="2821f-110">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2821f-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="2821f-111">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2821f-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="2821f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2821f-112">EXAMPLES</span></span>

### <span data-ttu-id="2821f-113">Get1</span><span class="sxs-lookup"><span data-stu-id="2821f-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="2821f-114">"Test" kaynak grubu altındaki "test" adlı dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="2821f-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="2821f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2821f-115">PARAMETERS</span></span>

### <span data-ttu-id="2821f-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="2821f-116">-ApiVersion</span></span>
<span data-ttu-id="2821f-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="2821f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2821f-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2821f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2821f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2821f-119">-DefaultProfile</span></span>
<span data-ttu-id="2821f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2821f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2821f-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="2821f-121">-DeploymentName</span></span>
<span data-ttu-id="2821f-122">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="2821f-122">The deployment name.</span></span>

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

### <span data-ttu-id="2821f-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2821f-123">-InformationAction</span></span>
<span data-ttu-id="2821f-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2821f-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2821f-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2821f-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2821f-126">'A</span><span class="sxs-lookup"><span data-stu-id="2821f-126">Continue</span></span>
- <span data-ttu-id="2821f-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="2821f-127">Ignore</span></span>
- <span data-ttu-id="2821f-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2821f-128">Inquire</span></span>
- <span data-ttu-id="2821f-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2821f-129">SilentlyContinue</span></span>
- <span data-ttu-id="2821f-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2821f-130">Stop</span></span>
- <span data-ttu-id="2821f-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2821f-131">Suspend</span></span>

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

### <span data-ttu-id="2821f-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2821f-132">-InformationVariable</span></span>
<span data-ttu-id="2821f-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2821f-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2821f-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="2821f-134">-Pre</span></span>
<span data-ttu-id="2821f-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2821f-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2821f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2821f-136">-ResourceGroupName</span></span>
<span data-ttu-id="2821f-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2821f-137">The resource group name.</span></span>

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

### <span data-ttu-id="2821f-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2821f-138">-SubscriptionId</span></span>
<span data-ttu-id="2821f-139">Kullanılacak abonelik.</span><span class="sxs-lookup"><span data-stu-id="2821f-139">The subscription to use.</span></span>

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

### <span data-ttu-id="2821f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2821f-140">CommonParameters</span></span>
<span data-ttu-id="2821f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2821f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2821f-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2821f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2821f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2821f-143">INPUTS</span></span>

## <span data-ttu-id="2821f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2821f-144">OUTPUTS</span></span>

## <span data-ttu-id="2821f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2821f-145">NOTES</span></span>

## <span data-ttu-id="2821f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2821f-146">RELATED LINKS</span></span>
