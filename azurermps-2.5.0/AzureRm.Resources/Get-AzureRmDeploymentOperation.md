---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 2bb5c3823d974dad53045d9283099befd4d60855
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940008"
---
# <span data-ttu-id="bf013-101">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf013-101">Get-AzureRmDeploymentOperation</span></span>

## <span data-ttu-id="bf013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf013-102">SYNOPSIS</span></span>
<span data-ttu-id="bf013-103">Dağıtım işlemini alma</span><span class="sxs-lookup"><span data-stu-id="bf013-103">Get deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf013-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf013-104">SYNTAX</span></span>

### <span data-ttu-id="bf013-105">GetByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf013-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf013-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="bf013-106">GetByDeploymentObject</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf013-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf013-107">DESCRIPTION</span></span>
<span data-ttu-id="bf013-108">**Get-AzureRmDeploymentOperation** cmdlet 'i, belirli bir dağıtımın başarısız olduğu tam işlemlerle ilgili daha fazla bilgi tanımlamanıza yardımcı olması için bir dağıtımın parçası olan tüm işlemleri listeler.</span><span class="sxs-lookup"><span data-stu-id="bf013-108">The **Get-AzureRmDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="bf013-109">Ayrıca, her dağıtım işlemi için yanıt ve istek içeriğini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="bf013-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="bf013-110">Bu, portalın dağıtım bilgilerinde sağlanan bilgilerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="bf013-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="bf013-111">İsteği ve yanıt içeriğini almak için, **Yeni-AzureRmDeployment** aracılığıyla dağıtım gönderirken ayarı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="bf013-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmDeployment**.</span></span>
<span data-ttu-id="bf013-112">Bu, dağıtım işlemlerini aldığınızda döndürülen kaynak özelliğinde veya **ListKeys** işlemlerinde kullanılan parolalar gibi gizli kod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="bf013-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="bf013-113">Bu ayar ve nasıl etkinleştirileceği ile ilgili daha fazla bilgi için New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="bf013-113">For more on this setting and how to enable it, see New-AzureRmDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="bf013-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf013-114">EXAMPLES</span></span>

### <span data-ttu-id="bf013-115">Dağıtım adı verilen dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="bf013-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

<span data-ttu-id="bf013-116">Geçerli abonelik kapsamındaki "test" adlı dağıtım işlemini alır.</span><span class="sxs-lookup"><span data-stu-id="bf013-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="bf013-117">Dağıtım alma ve dağıtım işlemlerini alma</span><span class="sxs-lookup"><span data-stu-id="bf013-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

<span data-ttu-id="bf013-118">Bu komut, geçerli abonelik kapsamındaki "test" dağıtımını alır ve dağıtım işlemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="bf013-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="bf013-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf013-119">PARAMETERS</span></span>

### <span data-ttu-id="bf013-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="bf013-120">-ApiVersion</span></span>
<span data-ttu-id="bf013-121">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf013-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bf013-122">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bf013-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bf013-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf013-123">-DefaultProfile</span></span>
<span data-ttu-id="bf013-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf013-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf013-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bf013-125">-DeploymentName</span></span>
<span data-ttu-id="bf013-126">Dağıtım adı.</span><span class="sxs-lookup"><span data-stu-id="bf013-126">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf013-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="bf013-127">-DeploymentObject</span></span>
<span data-ttu-id="bf013-128">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bf013-128">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf013-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bf013-129">-OperationId</span></span>
<span data-ttu-id="bf013-130">Dağıtım işlemi kimliği.</span><span class="sxs-lookup"><span data-stu-id="bf013-130">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf013-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="bf013-131">-Pre</span></span>
<span data-ttu-id="bf013-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf013-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bf013-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf013-133">CommonParameters</span></span>
<span data-ttu-id="bf013-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf013-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf013-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf013-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf013-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf013-136">INPUTS</span></span>

### <span data-ttu-id="bf013-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bf013-137">System.String</span></span>
<span data-ttu-id="bf013-138">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bf013-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bf013-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf013-139">OUTPUTS</span></span>

### <span data-ttu-id="bf013-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bf013-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="bf013-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf013-141">NOTES</span></span>

## <span data-ttu-id="bf013-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf013-142">RELATED LINKS</span></span>
