---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109989"
---
# <span data-ttu-id="6b13c-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6b13c-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="6b13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b13c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b13c-103">IoT Hub aygıtını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6b13c-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="6b13c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b13c-104">SYNTAX</span></span>

### <span data-ttu-id="6b13c-105">ResourceSetForStatus (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b13c-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-106">Inputobjectsetforauth</span><span class="sxs-lookup"><span data-stu-id="6b13c-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-107">Inputobjectsetforstatus</span><span class="sxs-lookup"><span data-stu-id="6b13c-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-108">Inputobjectsetforedgeenabled</span><span class="sxs-lookup"><span data-stu-id="6b13c-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="6b13c-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b13c-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6b13c-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-111">Resourceıdsetforauth</span><span class="sxs-lookup"><span data-stu-id="6b13c-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-112">Resourceıdsetforstatus</span><span class="sxs-lookup"><span data-stu-id="6b13c-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b13c-113">Resourceıdsetforedgeenabled</span><span class="sxs-lookup"><span data-stu-id="6b13c-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b13c-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b13c-114">DESCRIPTION</span></span>
<span data-ttu-id="6b13c-115">IoT Hub aygıtını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6b13c-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="6b13c-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b13c-116">EXAMPLES</span></span>

### <span data-ttu-id="6b13c-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6b13c-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="6b13c-118">Cihaz için Edge özelliklerini açma.</span><span class="sxs-lookup"><span data-stu-id="6b13c-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="6b13c-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6b13c-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="6b13c-120">Cihaz durumunu devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="6b13c-120">Disable device status.</span></span>

### <span data-ttu-id="6b13c-121">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6b13c-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="6b13c-122">IoT Hub aygıtının Yetkilendirme türünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="6b13c-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="6b13c-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b13c-123">PARAMETERS</span></span>

### <span data-ttu-id="6b13c-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="6b13c-124">-AuthMethod</span></span>
<span data-ttu-id="6b13c-125">Varlığın oluşturulduğu yetkilendirme türü.</span><span class="sxs-lookup"><span data-stu-id="6b13c-125">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="6b13c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b13c-126">-DefaultProfile</span></span>
<span data-ttu-id="6b13c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b13c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b13c-128">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="6b13c-128">-DeviceId</span></span>
<span data-ttu-id="6b13c-129">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="6b13c-129">Target Device Id.</span></span>

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

### <span data-ttu-id="6b13c-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6b13c-130">-EdgeEnabled</span></span>
<span data-ttu-id="6b13c-131">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="6b13c-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="6b13c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b13c-132">-InputObject</span></span>
<span data-ttu-id="6b13c-133">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="6b13c-133">IotHub object</span></span>

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

### <span data-ttu-id="6b13c-134">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="6b13c-134">-IotHubName</span></span>
<span data-ttu-id="6b13c-135">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="6b13c-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6b13c-136">-Primaryizizi</span><span class="sxs-lookup"><span data-stu-id="6b13c-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="6b13c-137">Birincil anahtar için kullanılmak üzere otomatik olarak imzalanan açık sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="6b13c-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="6b13c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b13c-138">-ResourceGroupName</span></span>
<span data-ttu-id="6b13c-139">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6b13c-139">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6b13c-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6b13c-140">-ResourceId</span></span>
<span data-ttu-id="6b13c-141">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6b13c-141">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6b13c-142">-Secondaryparmak Izi</span><span class="sxs-lookup"><span data-stu-id="6b13c-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="6b13c-143">İkincil anahtar için kullanılacak açık kendinden imzalanan sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="6b13c-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="6b13c-144">-Durum</span><span class="sxs-lookup"><span data-stu-id="6b13c-144">-Status</span></span>
<span data-ttu-id="6b13c-145">Oluşturma sırasında cihaz durumunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6b13c-145">Set device status upon creation.</span></span>

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

### <span data-ttu-id="6b13c-146">-Durumnedeni</span><span class="sxs-lookup"><span data-stu-id="6b13c-146">-StatusReason</span></span>
<span data-ttu-id="6b13c-147">Cihaz durumu açıklaması.</span><span class="sxs-lookup"><span data-stu-id="6b13c-147">Description for device status.</span></span>

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

### <span data-ttu-id="6b13c-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b13c-148">-Confirm</span></span>
<span data-ttu-id="6b13c-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b13c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b13c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b13c-150">-WhatIf</span></span>
<span data-ttu-id="6b13c-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b13c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b13c-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b13c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b13c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b13c-153">CommonParameters</span></span>
<span data-ttu-id="6b13c-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b13c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b13c-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b13c-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b13c-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b13c-156">INPUTS</span></span>

### <span data-ttu-id="6b13c-157">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="6b13c-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6b13c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6b13c-158">System.String</span></span>

## <span data-ttu-id="6b13c-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b13c-159">OUTPUTS</span></span>

### <span data-ttu-id="6b13c-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevme</span><span class="sxs-lookup"><span data-stu-id="6b13c-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="6b13c-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b13c-161">NOTES</span></span>

## <span data-ttu-id="6b13c-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b13c-162">RELATED LINKS</span></span>
