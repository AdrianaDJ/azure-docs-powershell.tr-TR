---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096896"
---
# <span data-ttu-id="757c8-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="757c8-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="757c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="757c8-102">SYNOPSIS</span></span>
<span data-ttu-id="757c8-103">IoT Hub aygıtını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="757c8-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="757c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="757c8-104">SYNTAX</span></span>

### <span data-ttu-id="757c8-105">ResourceSetForStatus (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="757c8-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-106">Inputobjectsetforauth</span><span class="sxs-lookup"><span data-stu-id="757c8-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-107">Inputobjectsetforstatus</span><span class="sxs-lookup"><span data-stu-id="757c8-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-108">Inputobjectsetforedgeenabled</span><span class="sxs-lookup"><span data-stu-id="757c8-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="757c8-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="757c8-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="757c8-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-111">Resourceıdsetforauth</span><span class="sxs-lookup"><span data-stu-id="757c8-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-112">Resourceıdsetforstatus</span><span class="sxs-lookup"><span data-stu-id="757c8-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757c8-113">Resourceıdsetforedgeenabled</span><span class="sxs-lookup"><span data-stu-id="757c8-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757c8-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="757c8-114">DESCRIPTION</span></span>
<span data-ttu-id="757c8-115">IoT Hub aygıtını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="757c8-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="757c8-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="757c8-116">EXAMPLES</span></span>

### <span data-ttu-id="757c8-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="757c8-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="757c8-118">Cihaz için Edge özelliklerini açma.</span><span class="sxs-lookup"><span data-stu-id="757c8-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="757c8-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="757c8-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="757c8-120">Cihaz durumunu devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="757c8-120">Disable device status.</span></span>

### <span data-ttu-id="757c8-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="757c8-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="757c8-122">IoT Hub aygıtının Yetkilendirme türünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="757c8-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="757c8-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="757c8-123">PARAMETERS</span></span>

### <span data-ttu-id="757c8-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="757c8-124">-AuthMethod</span></span>
<span data-ttu-id="757c8-125">Varlığın oluşturulduğu yetkilendirme türü.</span><span class="sxs-lookup"><span data-stu-id="757c8-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757c8-126">-DefaultProfile</span></span>
<span data-ttu-id="757c8-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="757c8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="757c8-128">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="757c8-128">-DeviceId</span></span>
<span data-ttu-id="757c8-129">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="757c8-129">Target Device Id.</span></span>

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

### <span data-ttu-id="757c8-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="757c8-130">-EdgeEnabled</span></span>
<span data-ttu-id="757c8-131">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="757c8-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="757c8-132">-InputObject</span></span>
<span data-ttu-id="757c8-133">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="757c8-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-134">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="757c8-134">-IotHubName</span></span>
<span data-ttu-id="757c8-135">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="757c8-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-136">-Primaryizizi</span><span class="sxs-lookup"><span data-stu-id="757c8-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="757c8-137">Birincil anahtar için kullanılmak üzere otomatik olarak imzalanan açık sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="757c8-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757c8-138">-ResourceGroupName</span></span>
<span data-ttu-id="757c8-139">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="757c8-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="757c8-140">-ResourceId</span></span>
<span data-ttu-id="757c8-141">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="757c8-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-142">-Secondaryparmak Izi</span><span class="sxs-lookup"><span data-stu-id="757c8-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="757c8-143">İkincil anahtar için kullanılacak açık kendinden imzalanan sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="757c8-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-144">-Durum</span><span class="sxs-lookup"><span data-stu-id="757c8-144">-Status</span></span>
<span data-ttu-id="757c8-145">Oluşturma sırasında cihaz durumunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="757c8-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-146">-Durumnedeni</span><span class="sxs-lookup"><span data-stu-id="757c8-146">-StatusReason</span></span>
<span data-ttu-id="757c8-147">Cihaz durumu açıklaması.</span><span class="sxs-lookup"><span data-stu-id="757c8-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757c8-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="757c8-148">-Confirm</span></span>
<span data-ttu-id="757c8-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="757c8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757c8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757c8-150">-WhatIf</span></span>
<span data-ttu-id="757c8-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="757c8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757c8-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="757c8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757c8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757c8-153">CommonParameters</span></span>
<span data-ttu-id="757c8-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="757c8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757c8-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757c8-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757c8-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="757c8-156">INPUTS</span></span>

### <span data-ttu-id="757c8-157">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="757c8-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="757c8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="757c8-158">System.String</span></span>

## <span data-ttu-id="757c8-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="757c8-159">OUTPUTS</span></span>

### <span data-ttu-id="757c8-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevme</span><span class="sxs-lookup"><span data-stu-id="757c8-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="757c8-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="757c8-161">NOTES</span></span>

## <span data-ttu-id="757c8-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="757c8-162">RELATED LINKS</span></span>
