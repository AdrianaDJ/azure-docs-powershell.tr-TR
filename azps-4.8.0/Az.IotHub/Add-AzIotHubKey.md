---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 422eb25456beb57ed6ab029fa5d70a47061ca491
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267441"
---
# <span data-ttu-id="9ddc2-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="9ddc2-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="9ddc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ddc2-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddc2-103">IotHub anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="9ddc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ddc2-104">SYNTAX</span></span>

### <span data-ttu-id="9ddc2-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ddc2-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ddc2-106">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9ddc2-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ddc2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ddc2-107">DESCRIPTION</span></span>
<span data-ttu-id="9ddc2-108">Sağlanan IotHub için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="9ddc2-109">KeyNames benzersiz değildir ve dikkatle yönetilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="9ddc2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ddc2-110">EXAMPLES</span></span>

### <span data-ttu-id="9ddc2-111">Örnek 1 bir IotHub anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="9ddc2-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="9ddc2-112">RegistryRead izinleriyle iothub "myiothub" adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="9ddc2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ddc2-113">PARAMETERS</span></span>

### <span data-ttu-id="9ddc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddc2-114">-DefaultProfile</span></span>
<span data-ttu-id="9ddc2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9ddc2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ddc2-116">-Hubıd</span><span class="sxs-lookup"><span data-stu-id="9ddc2-116">-HubId</span></span>
<span data-ttu-id="9ddc2-117">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9ddc2-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9ddc2-118">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="9ddc2-118">-KeyName</span></span>
<span data-ttu-id="9ddc2-119">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="9ddc2-119">Name of the Key</span></span>

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

### <span data-ttu-id="9ddc2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ddc2-120">-Name</span></span>
<span data-ttu-id="9ddc2-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="9ddc2-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddc2-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9ddc2-122">-PrimaryKey</span></span>
<span data-ttu-id="9ddc2-123">Birincil anahtar</span><span class="sxs-lookup"><span data-stu-id="9ddc2-123">The primary key</span></span>

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

### <span data-ttu-id="9ddc2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ddc2-124">-ResourceGroupName</span></span>
<span data-ttu-id="9ddc2-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9ddc2-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddc2-126">-Hak</span><span class="sxs-lookup"><span data-stu-id="9ddc2-126">-Rights</span></span>
<span data-ttu-id="9ddc2-127">Bu IOTHub için izinler</span><span class="sxs-lookup"><span data-stu-id="9ddc2-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddc2-128">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="9ddc2-128">-SecondaryKey</span></span>
<span data-ttu-id="9ddc2-129">Ikincil anahtar</span><span class="sxs-lookup"><span data-stu-id="9ddc2-129">The Secondary Key</span></span>

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

### <span data-ttu-id="9ddc2-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ddc2-130">-Confirm</span></span>
<span data-ttu-id="9ddc2-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddc2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ddc2-132">-WhatIf</span></span>
<span data-ttu-id="9ddc2-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ddc2-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddc2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddc2-135">CommonParameters</span></span>
<span data-ttu-id="9ddc2-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ddc2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddc2-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddc2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddc2-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ddc2-138">INPUTS</span></span>

### <span data-ttu-id="9ddc2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ddc2-139">System.String</span></span>

## <span data-ttu-id="9ddc2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ddc2-140">OUTPUTS</span></span>

### <span data-ttu-id="9ddc2-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="9ddc2-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="9ddc2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ddc2-142">NOTES</span></span>

## <span data-ttu-id="9ddc2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ddc2-143">RELATED LINKS</span></span>
