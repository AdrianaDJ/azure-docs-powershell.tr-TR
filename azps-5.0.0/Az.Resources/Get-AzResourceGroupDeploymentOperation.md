---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322948"
---
# <span data-ttu-id="5cd40-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5cd40-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="5cd40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd40-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd40-103">Kaynak grubu dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="5cd40-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="5cd40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cd40-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cd40-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cd40-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd40-106">**Get-AzResourceGroupDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="5cd40-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="5cd40-107">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="5cd40-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="5cd40-108">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="5cd40-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="5cd40-109">İsteği ve yanıt içeriğini almak için, **Yeni-AzResourceGroupDeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="5cd40-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="5cd40-110">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5cd40-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="5cd40-111">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5cd40-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="5cd40-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cd40-112">EXAMPLES</span></span>

### <span data-ttu-id="5cd40-113">Örnek 1: Get1</span><span class="sxs-lookup"><span data-stu-id="5cd40-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="5cd40-114">"Test" kaynak grubu altındaki "test" adlı dağıtım işlemini alır</span><span class="sxs-lookup"><span data-stu-id="5cd40-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="5cd40-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cd40-115">PARAMETERS</span></span>

### <span data-ttu-id="5cd40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd40-116">-DefaultProfile</span></span>
<span data-ttu-id="5cd40-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cd40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cd40-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5cd40-118">-DeploymentName</span></span>
<span data-ttu-id="5cd40-119">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="5cd40-119">The deployment name.</span></span>

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

### <span data-ttu-id="5cd40-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="5cd40-120">-Pre</span></span>
<span data-ttu-id="5cd40-121">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cd40-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5cd40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd40-122">-ResourceGroupName</span></span>
<span data-ttu-id="5cd40-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5cd40-123">The resource group name.</span></span>

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

### <span data-ttu-id="5cd40-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5cd40-124">-SubscriptionId</span></span>
<span data-ttu-id="5cd40-125">Kullanılacak abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cd40-125">The subscription to use.</span></span>

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

### <span data-ttu-id="5cd40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd40-126">CommonParameters</span></span>
<span data-ttu-id="5cd40-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cd40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd40-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5cd40-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd40-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cd40-129">INPUTS</span></span>

### <span data-ttu-id="5cd40-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5cd40-130">System.String</span></span>

### <span data-ttu-id="5cd40-131">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5cd40-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5cd40-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cd40-132">OUTPUTS</span></span>

### <span data-ttu-id="5cd40-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5cd40-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="5cd40-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cd40-134">NOTES</span></span>

## <span data-ttu-id="5cd40-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cd40-135">RELATED LINKS</span></span>
