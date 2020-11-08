---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 5a5a1134687a5a08b8f00e383105ad9c0a1a2d4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108050"
---
# <span data-ttu-id="ccca4-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ccca4-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="ccca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccca4-102">SYNOPSIS</span></span>
<span data-ttu-id="ccca4-103">Kaynak grubu dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="ccca4-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="ccca4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccca4-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccca4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccca4-105">DESCRIPTION</span></span>
<span data-ttu-id="ccca4-106">**Get-AzResourceGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="ccca4-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="ccca4-107">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="ccca4-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="ccca4-108">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="ccca4-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="ccca4-109">İsteği ve yanıt içeriğini almak için, **Yeni-AzResourceGroupDeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ccca4-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="ccca4-110">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="ccca4-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="ccca4-111">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ccca4-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="ccca4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccca4-112">EXAMPLES</span></span>

### <span data-ttu-id="ccca4-113">Örnek 1: Get1</span><span class="sxs-lookup"><span data-stu-id="ccca4-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="ccca4-114">"Test" kaynak grubu altındaki "test" adlı dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="ccca4-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="ccca4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccca4-115">PARAMETERS</span></span>

### <span data-ttu-id="ccca4-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ccca4-116">-ApiVersion</span></span>
<span data-ttu-id="ccca4-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccca4-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ccca4-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ccca4-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ccca4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccca4-119">-DefaultProfile</span></span>
<span data-ttu-id="ccca4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccca4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccca4-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="ccca4-121">-DeploymentName</span></span>
<span data-ttu-id="ccca4-122">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="ccca4-122">The deployment name.</span></span>

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

### <span data-ttu-id="ccca4-123">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ccca4-123">-Pre</span></span>
<span data-ttu-id="ccca4-124">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccca4-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ccca4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccca4-125">-ResourceGroupName</span></span>
<span data-ttu-id="ccca4-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ccca4-126">The resource group name.</span></span>

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

### <span data-ttu-id="ccca4-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ccca4-127">-SubscriptionId</span></span>
<span data-ttu-id="ccca4-128">Kullanılacak abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccca4-128">The subscription to use.</span></span>

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

### <span data-ttu-id="ccca4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccca4-129">CommonParameters</span></span>
<span data-ttu-id="ccca4-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccca4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccca4-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ccca4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccca4-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccca4-132">INPUTS</span></span>

### <span data-ttu-id="ccca4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ccca4-133">System.String</span></span>

### <span data-ttu-id="ccca4-134">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ccca4-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ccca4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccca4-135">OUTPUTS</span></span>

### <span data-ttu-id="ccca4-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ccca4-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ccca4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccca4-137">NOTES</span></span>

## <span data-ttu-id="ccca4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccca4-138">RELATED LINKS</span></span>
