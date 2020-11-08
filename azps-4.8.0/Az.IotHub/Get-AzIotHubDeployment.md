---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273558"
---
# <span data-ttu-id="31eec-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="31eec-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="31eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31eec-102">SYNOPSIS</span></span>
<span data-ttu-id="31eec-103">Tüm veya belirli bir IoT Edge dağıtımını listeler.</span><span class="sxs-lookup"><span data-stu-id="31eec-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="31eec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31eec-104">SYNTAX</span></span>

### <span data-ttu-id="31eec-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31eec-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31eec-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="31eec-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31eec-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="31eec-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31eec-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="31eec-108">DESCRIPTION</span></span>
<span data-ttu-id="31eec-109">IoT Hub 'ındaki bir IoT uç dağıtımının veya liste IoT uç dağıtımlarının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="31eec-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="31eec-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="31eec-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="31eec-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31eec-111">EXAMPLES</span></span>

### <span data-ttu-id="31eec-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31eec-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="31eec-113">IoT Edge dağıtımının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="31eec-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="31eec-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="31eec-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="31eec-115">IoT Hub 'ındaki tüm IoT Edge dağıtımlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="31eec-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="31eec-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31eec-116">PARAMETERS</span></span>

### <span data-ttu-id="31eec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31eec-117">-DefaultProfile</span></span>
<span data-ttu-id="31eec-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31eec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31eec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31eec-119">-InputObject</span></span>
<span data-ttu-id="31eec-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="31eec-120">IotHub object</span></span>

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

### <span data-ttu-id="31eec-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="31eec-121">-IotHubName</span></span>
<span data-ttu-id="31eec-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="31eec-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="31eec-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="31eec-123">-Name</span></span>
<span data-ttu-id="31eec-124">Dağıtımın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="31eec-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="31eec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31eec-125">-ResourceGroupName</span></span>
<span data-ttu-id="31eec-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="31eec-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="31eec-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="31eec-127">-ResourceId</span></span>
<span data-ttu-id="31eec-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="31eec-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="31eec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31eec-129">CommonParameters</span></span>
<span data-ttu-id="31eec-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31eec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31eec-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31eec-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31eec-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31eec-132">INPUTS</span></span>

### <span data-ttu-id="31eec-133">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="31eec-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="31eec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="31eec-134">System.String</span></span>

## <span data-ttu-id="31eec-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31eec-135">OUTPUTS</span></span>

### <span data-ttu-id="31eec-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="31eec-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="31eec-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="31eec-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="31eec-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31eec-138">NOTES</span></span>

## <span data-ttu-id="31eec-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31eec-139">RELATED LINKS</span></span>
