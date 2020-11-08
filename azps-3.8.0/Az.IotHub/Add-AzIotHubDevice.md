---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104341"
---
# <span data-ttu-id="e0503-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="e0503-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="e0503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0503-102">SYNOPSIS</span></span>
<span data-ttu-id="e0503-103">IoT merkezinde bir cihaz oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0503-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="e0503-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0503-104">SYNTAX</span></span>

### <span data-ttu-id="e0503-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0503-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0503-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="e0503-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0503-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e0503-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0503-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0503-108">DESCRIPTION</span></span>
<span data-ttu-id="e0503-109">IoT Hub 'ında farklı kimlik doğrulama türüne sahip bir cihaz oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0503-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="e0503-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0503-110">EXAMPLES</span></span>

### <span data-ttu-id="e0503-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0503-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="e0503-112">Varsayılan yetkilendirmeyi (paylaşılan özel anahtarı) içeren bir Edge uyumlu IoT cihazı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0503-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="e0503-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e0503-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="e0503-114">Devre dışı durumu ve nedeni olan kök CA yetkilendirmesi içeren bir IoT cihazı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e0503-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="e0503-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e0503-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="e0503-116">Edge 'in etkinleştirildiği bir IoT cihazı oluşturun ve buna alt aygıtlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e0503-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="e0503-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="e0503-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="e0503-118">IoT cihazı oluşturun ve ana aygıtını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e0503-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="e0503-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0503-119">PARAMETERS</span></span>

### <span data-ttu-id="e0503-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="e0503-120">-AuthMethod</span></span>
<span data-ttu-id="e0503-121">Varlığın oluşturulduğu yetkilendirme türü.</span><span class="sxs-lookup"><span data-stu-id="e0503-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="e0503-122">-Çocuklar</span><span class="sxs-lookup"><span data-stu-id="e0503-122">-Children</span></span>
<span data-ttu-id="e0503-123">Alt cihaz listesi (virgülle ayrılmış) Ekle yalnızca kenara ait olmayan cihazları içerir.</span><span class="sxs-lookup"><span data-stu-id="e0503-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0503-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0503-124">-DefaultProfile</span></span>
<span data-ttu-id="e0503-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0503-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0503-126">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="e0503-126">-DeviceId</span></span>
<span data-ttu-id="e0503-127">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="e0503-127">Target Device Id.</span></span>

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

### <span data-ttu-id="e0503-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="e0503-128">-EdgeEnabled</span></span>
<span data-ttu-id="e0503-129">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="e0503-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="e0503-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e0503-130">-Force</span></span>
<span data-ttu-id="e0503-131">Kenar Çizgili olmayan cihazın üst aygıtının üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="e0503-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="e0503-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0503-132">-InputObject</span></span>
<span data-ttu-id="e0503-133">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="e0503-133">IotHub object</span></span>

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

### <span data-ttu-id="e0503-134">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="e0503-134">-IotHubName</span></span>
<span data-ttu-id="e0503-135">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="e0503-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e0503-136">-Primaryizizi</span><span class="sxs-lookup"><span data-stu-id="e0503-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="e0503-137">Birincil anahtar için kullanılmak üzere otomatik olarak imzalanan açık sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="e0503-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="e0503-138">-Parentdeviceıd</span><span class="sxs-lookup"><span data-stu-id="e0503-138">-ParentDeviceId</span></span>
<span data-ttu-id="e0503-139">Sınır aygıtının kimliği.</span><span class="sxs-lookup"><span data-stu-id="e0503-139">Id of edge device.</span></span>

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

### <span data-ttu-id="e0503-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0503-140">-ResourceGroupName</span></span>
<span data-ttu-id="e0503-141">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e0503-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e0503-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e0503-142">-ResourceId</span></span>
<span data-ttu-id="e0503-143">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e0503-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e0503-144">-Secondaryparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e0503-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="e0503-145">İkincil anahtar için kullanılacak açık kendinden imzalanan sertifika parmak izi.</span><span class="sxs-lookup"><span data-stu-id="e0503-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="e0503-146">-Durum</span><span class="sxs-lookup"><span data-stu-id="e0503-146">-Status</span></span>
<span data-ttu-id="e0503-147">Oluşturma sırasında cihaz durumunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e0503-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0503-148">-Durumnedeni</span><span class="sxs-lookup"><span data-stu-id="e0503-148">-StatusReason</span></span>
<span data-ttu-id="e0503-149">Cihaz durumu açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e0503-149">Description for device status.</span></span>

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

### <span data-ttu-id="e0503-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0503-150">-Confirm</span></span>
<span data-ttu-id="e0503-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0503-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0503-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0503-152">-WhatIf</span></span>
<span data-ttu-id="e0503-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0503-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0503-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0503-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0503-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0503-155">CommonParameters</span></span>
<span data-ttu-id="e0503-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0503-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0503-157">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0503-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0503-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0503-158">INPUTS</span></span>

### <span data-ttu-id="e0503-159">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="e0503-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e0503-160">System. String</span><span class="sxs-lookup"><span data-stu-id="e0503-160">System.String</span></span>

## <span data-ttu-id="e0503-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0503-161">OUTPUTS</span></span>

### <span data-ttu-id="e0503-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevme</span><span class="sxs-lookup"><span data-stu-id="e0503-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="e0503-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0503-163">NOTES</span></span>

## <span data-ttu-id="e0503-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0503-164">RELATED LINKS</span></span>
