---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593117"
---
# <span data-ttu-id="6c62a-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="6c62a-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="6c62a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c62a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c62a-103">IotHub anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c62a-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c62a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c62a-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c62a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c62a-105">DESCRIPTION</span></span>
<span data-ttu-id="6c62a-106">Sağlanan IotHub için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c62a-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="6c62a-107">KeyNames benzersiz değildir ve dikkatle yönetilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6c62a-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="6c62a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c62a-108">EXAMPLES</span></span>

### <span data-ttu-id="6c62a-109">Örnek 1 bir IotHub anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="6c62a-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="6c62a-110">RegistryRead izinleriyle iothub "myiothub" adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c62a-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="6c62a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c62a-111">PARAMETERS</span></span>

### <span data-ttu-id="6c62a-112">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="6c62a-112">-KeyName</span></span>
<span data-ttu-id="6c62a-113">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="6c62a-113">Name of the Key</span></span>

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

### <span data-ttu-id="6c62a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c62a-114">-Name</span></span>
<span data-ttu-id="6c62a-115">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="6c62a-115">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c62a-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="6c62a-116">-PrimaryKey</span></span>
<span data-ttu-id="6c62a-117">Birincil anahtar</span><span class="sxs-lookup"><span data-stu-id="6c62a-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c62a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c62a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6c62a-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6c62a-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c62a-120">-Hak</span><span class="sxs-lookup"><span data-stu-id="6c62a-120">-Rights</span></span>
<span data-ttu-id="6c62a-121">Bu IOTHub için izinler</span><span class="sxs-lookup"><span data-stu-id="6c62a-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c62a-122">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="6c62a-122">-SecondaryKey</span></span>
<span data-ttu-id="6c62a-123">Ikincil anahtar</span><span class="sxs-lookup"><span data-stu-id="6c62a-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c62a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c62a-124">-Confirm</span></span>
<span data-ttu-id="6c62a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c62a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c62a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c62a-126">-WhatIf</span></span>
<span data-ttu-id="6c62a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c62a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c62a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c62a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c62a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c62a-129">-DefaultProfile</span></span>
<span data-ttu-id="6c62a-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c62a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c62a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c62a-131">CommonParameters</span></span>
<span data-ttu-id="6c62a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c62a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c62a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c62a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c62a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c62a-134">INPUTS</span></span>

### <span data-ttu-id="6c62a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6c62a-135">System.String</span></span>
<span data-ttu-id="6c62a-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="6c62a-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="6c62a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c62a-137">OUTPUTS</span></span>

### <span data-ttu-id="6c62a-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="6c62a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="6c62a-139">System. Koleksiyonlar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstif, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="6c62a-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="6c62a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c62a-140">NOTES</span></span>

## <span data-ttu-id="6c62a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c62a-141">RELATED LINKS</span></span>

