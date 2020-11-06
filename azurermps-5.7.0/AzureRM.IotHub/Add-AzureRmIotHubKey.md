---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: c56b147c5ac62e376eff1159eb679c5a692eb1b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591679"
---
# <span data-ttu-id="ae456-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="ae456-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="ae456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae456-102">SYNOPSIS</span></span>
<span data-ttu-id="ae456-103">IotHub anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae456-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae456-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae456-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae456-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae456-105">DESCRIPTION</span></span>
<span data-ttu-id="ae456-106">Sağlanan IotHub için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae456-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="ae456-107">KeyNames benzersiz değildir ve dikkatle yönetilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ae456-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="ae456-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae456-108">EXAMPLES</span></span>

### <span data-ttu-id="ae456-109">Örnek 1 bir IotHub anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="ae456-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="ae456-110">RegistryRead izinleriyle iothub "myiothub" adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae456-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="ae456-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae456-111">PARAMETERS</span></span>

### <span data-ttu-id="ae456-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae456-112">-DefaultProfile</span></span>
<span data-ttu-id="ae456-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ae456-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="ae456-114">-KeyName</span></span>
<span data-ttu-id="ae456-115">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="ae456-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae456-116">-Name</span></span>
<span data-ttu-id="ae456-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="ae456-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ae456-118">-PrimaryKey</span></span>
<span data-ttu-id="ae456-119">Birincil anahtar</span><span class="sxs-lookup"><span data-stu-id="ae456-119">The primary key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae456-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae456-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ae456-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-122">-Hak</span><span class="sxs-lookup"><span data-stu-id="ae456-122">-Rights</span></span>
<span data-ttu-id="ae456-123">Bu IOTHub için izinler</span><span class="sxs-lookup"><span data-stu-id="ae456-123">The permissions for this IOTHub</span></span>

```yaml
Type: PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-124">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="ae456-124">-SecondaryKey</span></span>
<span data-ttu-id="ae456-125">Ikincil anahtar</span><span class="sxs-lookup"><span data-stu-id="ae456-125">The Secondary Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae456-126">-Confirm</span></span>
<span data-ttu-id="ae456-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae456-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae456-128">-WhatIf</span></span>
<span data-ttu-id="ae456-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae456-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae456-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae456-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae456-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae456-131">CommonParameters</span></span>
<span data-ttu-id="ae456-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae456-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae456-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae456-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae456-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae456-134">INPUTS</span></span>

### <span data-ttu-id="ae456-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ae456-135">System.String</span></span>
<span data-ttu-id="ae456-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="ae456-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="ae456-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae456-137">OUTPUTS</span></span>

### <span data-ttu-id="ae456-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="ae456-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="ae456-139">System. Koleksiyonlar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstif, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="ae456-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="ae456-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae456-140">NOTES</span></span>

## <span data-ttu-id="ae456-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae456-141">RELATED LINKS</span></span>

