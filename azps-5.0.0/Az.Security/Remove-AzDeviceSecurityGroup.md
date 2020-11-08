---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276732"
---
# <span data-ttu-id="b280c-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b280c-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="b280c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b280c-102">SYNOPSIS</span></span>
<span data-ttu-id="b280c-103">Cihaz güvenlik grubunu silme</span><span class="sxs-lookup"><span data-stu-id="b280c-103">Delete device security group</span></span>

## <span data-ttu-id="b280c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b280c-104">SYNTAX</span></span>

### <span data-ttu-id="b280c-105">Resourceıdlevelresource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b280c-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b280c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b280c-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b280c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b280c-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b280c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b280c-108">DESCRIPTION</span></span>
<span data-ttu-id="b280c-109">Remove-AzDeviceSecurityGroup cmdlet, IoT güvenlik çözümünde tanımlanan bir cihaz güvenlik grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="b280c-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="b280c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b280c-110">EXAMPLES</span></span>

### <span data-ttu-id="b280c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b280c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="b280c-112">"/Subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" kaynak kimliğiyle IoT Hub 'ın "Mysecuritgroup" cihaz güvenlik grubunu silme</span><span class="sxs-lookup"><span data-stu-id="b280c-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="b280c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b280c-113">PARAMETERS</span></span>

### <span data-ttu-id="b280c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b280c-114">-DefaultProfile</span></span>
<span data-ttu-id="b280c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b280c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b280c-116">-Hubresourceıd</span><span class="sxs-lookup"><span data-stu-id="b280c-116">-HubResourceId</span></span>
<span data-ttu-id="b280c-117">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b280c-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b280c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b280c-118">-InputObject</span></span>
<span data-ttu-id="b280c-119">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b280c-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b280c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b280c-120">-Name</span></span>
<span data-ttu-id="b280c-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="b280c-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b280c-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b280c-122">-PassThru</span></span>
<span data-ttu-id="b280c-123">İşlemin başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="b280c-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="b280c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b280c-124">-ResourceId</span></span>
<span data-ttu-id="b280c-125">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b280c-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b280c-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b280c-126">-Confirm</span></span>
<span data-ttu-id="b280c-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b280c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b280c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b280c-128">-WhatIf</span></span>
<span data-ttu-id="b280c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b280c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b280c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b280c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b280c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b280c-131">CommonParameters</span></span>
<span data-ttu-id="b280c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b280c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b280c-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b280c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b280c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b280c-134">INPUTS</span></span>

### <span data-ttu-id="b280c-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b280c-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="b280c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b280c-136">System.String</span></span>

## <span data-ttu-id="b280c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b280c-137">OUTPUTS</span></span>

### <span data-ttu-id="b280c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b280c-138">System.Boolean</span></span>

## <span data-ttu-id="b280c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b280c-139">NOTES</span></span>

## <span data-ttu-id="b280c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b280c-140">RELATED LINKS</span></span>
