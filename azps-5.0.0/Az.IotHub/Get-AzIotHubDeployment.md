---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277756"
---
# <span data-ttu-id="51626-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="51626-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="51626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51626-102">SYNOPSIS</span></span>
<span data-ttu-id="51626-103">Tüm veya belirli bir IoT Edge dağıtımını listeler.</span><span class="sxs-lookup"><span data-stu-id="51626-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="51626-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51626-104">SYNTAX</span></span>

### <span data-ttu-id="51626-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51626-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51626-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="51626-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51626-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="51626-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51626-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="51626-108">DESCRIPTION</span></span>
<span data-ttu-id="51626-109">IoT Hub 'ındaki bir IoT uç dağıtımının veya liste IoT uç dağıtımlarının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="51626-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="51626-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="51626-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="51626-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51626-111">EXAMPLES</span></span>

### <span data-ttu-id="51626-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51626-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="51626-113">IoT Edge dağıtımının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="51626-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="51626-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="51626-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="51626-115">IoT Hub 'ındaki tüm IoT Edge dağıtımlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="51626-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="51626-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51626-116">PARAMETERS</span></span>

### <span data-ttu-id="51626-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51626-117">-DefaultProfile</span></span>
<span data-ttu-id="51626-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51626-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51626-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51626-119">-InputObject</span></span>
<span data-ttu-id="51626-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="51626-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51626-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="51626-121">-IotHubName</span></span>
<span data-ttu-id="51626-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="51626-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51626-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="51626-123">-Name</span></span>
<span data-ttu-id="51626-124">Dağıtımın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="51626-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="51626-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51626-125">-ResourceGroupName</span></span>
<span data-ttu-id="51626-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="51626-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51626-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="51626-127">-ResourceId</span></span>
<span data-ttu-id="51626-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="51626-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51626-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51626-129">CommonParameters</span></span>
<span data-ttu-id="51626-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51626-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51626-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51626-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51626-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51626-132">INPUTS</span></span>

### <span data-ttu-id="51626-133">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="51626-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="51626-134">System. String</span><span class="sxs-lookup"><span data-stu-id="51626-134">System.String</span></span>

## <span data-ttu-id="51626-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51626-135">OUTPUTS</span></span>

### <span data-ttu-id="51626-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="51626-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="51626-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="51626-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="51626-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51626-138">NOTES</span></span>

## <span data-ttu-id="51626-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51626-139">RELATED LINKS</span></span>
