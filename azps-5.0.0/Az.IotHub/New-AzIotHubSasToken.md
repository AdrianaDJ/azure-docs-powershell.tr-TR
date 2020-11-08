---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277735"
---
# <span data-ttu-id="a5d7a-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="a5d7a-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="a5d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d7a-103">Hedef IoT Merkezi, cihaz veya modül için SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="a5d7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5d7a-104">SYNTAX</span></span>

### <span data-ttu-id="a5d7a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5d7a-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d7a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a5d7a-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d7a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a5d7a-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d7a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5d7a-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d7a-109">Cihaz SAS belirteçleri için, ilke parametresi yalnızca cihaz kayıt defterine erişmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="a5d7a-110">Bu nedenle ilkenin kayıt defterine okuma erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="a5d7a-111">IoT Hub belirteçleri için ilke SAS 'ın bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="a5d7a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5d7a-112">EXAMPLES</span></span>

### <span data-ttu-id="a5d7a-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5d7a-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="a5d7a-114">Iothubowner ilkesini ve birincil anahtarı kullanarak IoT merkezi SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="a5d7a-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a5d7a-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="a5d7a-116">RegistryRead ilkesini ve ikincil anahtarını kullanarak IoT merkezi SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="a5d7a-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a5d7a-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="a5d7a-118">{İothub_name} cihaz kayıt defterine erişmek için ıothubowner ilkesini kullanarak bir cihaz SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="a5d7a-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a5d7a-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="a5d7a-120">{İothub_name} cihaz kayıt defterine erişmek için ıothubowner ilkesini kullanarak bir modül SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="a5d7a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5d7a-121">PARAMETERS</span></span>

### <span data-ttu-id="a5d7a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d7a-122">-DefaultProfile</span></span>
<span data-ttu-id="a5d7a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d7a-124">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="a5d7a-124">-DeviceId</span></span>
<span data-ttu-id="a5d7a-125">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-125">Target Device Id.</span></span>

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

### <span data-ttu-id="a5d7a-126">-Süre</span><span class="sxs-lookup"><span data-stu-id="a5d7a-126">-Duration</span></span>
<span data-ttu-id="a5d7a-127">Oluşturulacak belirtecin gelecek süre sonu (saniye).</span><span class="sxs-lookup"><span data-stu-id="a5d7a-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="a5d7a-128">Varsayılan 3600 ' dır.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d7a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5d7a-129">-InputObject</span></span>
<span data-ttu-id="a5d7a-130">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="a5d7a-130">IotHub object</span></span>

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

### <span data-ttu-id="a5d7a-131">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="a5d7a-131">-IotHubName</span></span>
<span data-ttu-id="a5d7a-132">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="a5d7a-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a5d7a-133">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="a5d7a-133">-KeyName</span></span>
<span data-ttu-id="a5d7a-134">Access anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-134">Access key name.</span></span>

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

### <span data-ttu-id="a5d7a-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a5d7a-135">-KeyType</span></span>
<span data-ttu-id="a5d7a-136">Access anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d7a-137">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="a5d7a-137">-ModuleId</span></span>
<span data-ttu-id="a5d7a-138">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-138">Target Module Id.</span></span>

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

### <span data-ttu-id="a5d7a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d7a-139">-ResourceGroupName</span></span>
<span data-ttu-id="a5d7a-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a5d7a-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a5d7a-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5d7a-141">-ResourceId</span></span>
<span data-ttu-id="a5d7a-142">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a5d7a-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a5d7a-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5d7a-143">-Confirm</span></span>
<span data-ttu-id="a5d7a-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d7a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d7a-145">-WhatIf</span></span>
<span data-ttu-id="a5d7a-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d7a-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d7a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d7a-148">CommonParameters</span></span>
<span data-ttu-id="a5d7a-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5d7a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d7a-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d7a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d7a-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5d7a-151">INPUTS</span></span>

### <span data-ttu-id="a5d7a-152">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a5d7a-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a5d7a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d7a-153">System.String</span></span>

## <span data-ttu-id="a5d7a-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5d7a-154">OUTPUTS</span></span>

### <span data-ttu-id="a5d7a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d7a-155">System.String</span></span>

## <span data-ttu-id="a5d7a-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5d7a-156">NOTES</span></span>

## <span data-ttu-id="a5d7a-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5d7a-157">RELATED LINKS</span></span>
