---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 3505a2b18ac35644fe401dea4aca8c96b10a7f2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751773"
---
# <span data-ttu-id="b6c89-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b6c89-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="b6c89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6c89-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c89-103">IotHub anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6c89-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="b6c89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6c89-104">SYNTAX</span></span>

### <span data-ttu-id="b6c89-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6c89-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6c89-106">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b6c89-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6c89-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6c89-107">DESCRIPTION</span></span>
<span data-ttu-id="b6c89-108">Sağlanan IotHub için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6c89-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="b6c89-109">KeyNames benzersiz değildir ve dikkatle yönetilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b6c89-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="b6c89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6c89-110">EXAMPLES</span></span>

### <span data-ttu-id="b6c89-111">Örnek 1 bir IotHub anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="b6c89-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="b6c89-112">RegistryRead izinleriyle iothub "myiothub" adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b6c89-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="b6c89-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6c89-113">PARAMETERS</span></span>

### <span data-ttu-id="b6c89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c89-114">-DefaultProfile</span></span>
<span data-ttu-id="b6c89-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b6c89-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6c89-116">-Hubıd</span><span class="sxs-lookup"><span data-stu-id="b6c89-116">-HubId</span></span>
<span data-ttu-id="b6c89-117">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b6c89-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b6c89-118">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="b6c89-118">-KeyName</span></span>
<span data-ttu-id="b6c89-119">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="b6c89-119">Name of the Key</span></span>

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

### <span data-ttu-id="b6c89-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6c89-120">-Name</span></span>
<span data-ttu-id="b6c89-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="b6c89-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b6c89-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b6c89-122">-PrimaryKey</span></span>
<span data-ttu-id="b6c89-123">Birincil anahtar</span><span class="sxs-lookup"><span data-stu-id="b6c89-123">The primary key</span></span>

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

### <span data-ttu-id="b6c89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c89-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6c89-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b6c89-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b6c89-126">-Hak</span><span class="sxs-lookup"><span data-stu-id="b6c89-126">-Rights</span></span>
<span data-ttu-id="b6c89-127">Bu IOTHub için izinler</span><span class="sxs-lookup"><span data-stu-id="b6c89-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="b6c89-128">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="b6c89-128">-SecondaryKey</span></span>
<span data-ttu-id="b6c89-129">Ikincil anahtar</span><span class="sxs-lookup"><span data-stu-id="b6c89-129">The Secondary Key</span></span>

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

### <span data-ttu-id="b6c89-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6c89-130">-Confirm</span></span>
<span data-ttu-id="b6c89-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6c89-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c89-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c89-132">-WhatIf</span></span>
<span data-ttu-id="b6c89-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6c89-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6c89-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6c89-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c89-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c89-135">CommonParameters</span></span>
<span data-ttu-id="b6c89-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6c89-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c89-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6c89-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c89-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6c89-138">INPUTS</span></span>

### <span data-ttu-id="b6c89-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c89-139">System.String</span></span>

## <span data-ttu-id="b6c89-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6c89-140">OUTPUTS</span></span>

### <span data-ttu-id="b6c89-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="b6c89-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b6c89-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6c89-142">NOTES</span></span>

## <span data-ttu-id="b6c89-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6c89-143">RELATED LINKS</span></span>
