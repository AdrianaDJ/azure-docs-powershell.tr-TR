---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096875"
---
# <span data-ttu-id="b57b0-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="b57b0-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="b57b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b57b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b57b0-103">Bir IoT Hub 'ındaki hedef IoT aygıtındaki modülü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b57b0-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b57b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b57b0-104">SYNTAX</span></span>

### <span data-ttu-id="b57b0-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b57b0-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b57b0-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="b57b0-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b57b0-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b57b0-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b57b0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b57b0-108">DESCRIPTION</span></span>
<span data-ttu-id="b57b0-109">Bir IoT Hub 'ındaki hedef IoT aygıtındaki modülü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b57b0-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b57b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b57b0-110">EXAMPLES</span></span>

### <span data-ttu-id="b57b0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b57b0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="b57b0-112">IoT aygıt modülünün Yetkilendirme türünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b57b0-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="b57b0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b57b0-113">PARAMETERS</span></span>

### <span data-ttu-id="b57b0-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="b57b0-114">-AuthMethod</span></span>
<span data-ttu-id="b57b0-115">Varlığın oluşturulduğu yetkilendirme türü.</span><span class="sxs-lookup"><span data-stu-id="b57b0-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b57b0-116">-DefaultProfile</span></span>
<span data-ttu-id="b57b0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b57b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b57b0-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="b57b0-118">-DeviceId</span></span>
<span data-ttu-id="b57b0-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="b57b0-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57b0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b57b0-120">-InputObject</span></span>
<span data-ttu-id="b57b0-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="b57b0-121">IotHub object</span></span>

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

### <span data-ttu-id="b57b0-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="b57b0-122">-IotHubName</span></span>
<span data-ttu-id="b57b0-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="b57b0-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b57b0-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="b57b0-124">-ModuleId</span></span>
<span data-ttu-id="b57b0-125">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="b57b0-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57b0-126">-Primaryizizi</span><span class="sxs-lookup"><span data-stu-id="b57b0-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="b57b0-127">Birincil anahtar için kullanılmak üzere otomatik olarak imzalanan açık sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="b57b0-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="b57b0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b57b0-128">-ResourceGroupName</span></span>
<span data-ttu-id="b57b0-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b57b0-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b57b0-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b57b0-130">-ResourceId</span></span>
<span data-ttu-id="b57b0-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b57b0-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b57b0-132">-Secondaryparmak Izi</span><span class="sxs-lookup"><span data-stu-id="b57b0-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="b57b0-133">İkincil anahtar için kullanılacak açık kendinden imzalanan sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="b57b0-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b57b0-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b57b0-134">-Confirm</span></span>
<span data-ttu-id="b57b0-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b57b0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b57b0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b57b0-136">-WhatIf</span></span>
<span data-ttu-id="b57b0-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b57b0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b57b0-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b57b0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b57b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b57b0-139">CommonParameters</span></span>
<span data-ttu-id="b57b0-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b57b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b57b0-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b57b0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b57b0-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b57b0-142">INPUTS</span></span>

### <span data-ttu-id="b57b0-143">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="b57b0-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b57b0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b57b0-144">System.String</span></span>

## <span data-ttu-id="b57b0-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b57b0-145">OUTPUTS</span></span>

### <span data-ttu-id="b57b0-146">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModule</span><span class="sxs-lookup"><span data-stu-id="b57b0-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="b57b0-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b57b0-147">NOTES</span></span>

## <span data-ttu-id="b57b0-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b57b0-148">RELATED LINKS</span></span>