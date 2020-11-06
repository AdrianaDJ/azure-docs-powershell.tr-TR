---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590243"
---
# <span data-ttu-id="394cb-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="394cb-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="394cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394cb-102">SYNOPSIS</span></span>
<span data-ttu-id="394cb-103">IotHub anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="394cb-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="394cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="394cb-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="394cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="394cb-105">DESCRIPTION</span></span>
<span data-ttu-id="394cb-106">Sağlanan IotHub için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="394cb-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="394cb-107">KeyNames benzersiz değildir ve dikkatle yönetilmelidir.</span><span class="sxs-lookup"><span data-stu-id="394cb-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="394cb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="394cb-108">EXAMPLES</span></span>

### <span data-ttu-id="394cb-109">Örnek 1 bir IotHub anahtar ekleme</span><span class="sxs-lookup"><span data-stu-id="394cb-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="394cb-110">RegistryRead izinleriyle iothub "myiothub" adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="394cb-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="394cb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="394cb-111">PARAMETERS</span></span>

### <span data-ttu-id="394cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394cb-112">-DefaultProfile</span></span>
<span data-ttu-id="394cb-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="394cb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="394cb-114">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="394cb-114">-KeyName</span></span>
<span data-ttu-id="394cb-115">Anahtarın adı</span><span class="sxs-lookup"><span data-stu-id="394cb-115">Name of the Key</span></span>

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

### <span data-ttu-id="394cb-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="394cb-116">-Name</span></span>
<span data-ttu-id="394cb-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="394cb-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="394cb-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="394cb-118">-PrimaryKey</span></span>
<span data-ttu-id="394cb-119">Birincil anahtar</span><span class="sxs-lookup"><span data-stu-id="394cb-119">The primary key</span></span>

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

### <span data-ttu-id="394cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="394cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="394cb-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="394cb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="394cb-122">-Hak</span><span class="sxs-lookup"><span data-stu-id="394cb-122">-Rights</span></span>
<span data-ttu-id="394cb-123">Bu IOTHub için izinler</span><span class="sxs-lookup"><span data-stu-id="394cb-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="394cb-124">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="394cb-124">-SecondaryKey</span></span>
<span data-ttu-id="394cb-125">Ikincil anahtar</span><span class="sxs-lookup"><span data-stu-id="394cb-125">The Secondary Key</span></span>

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

### <span data-ttu-id="394cb-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="394cb-126">-Confirm</span></span>
<span data-ttu-id="394cb-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="394cb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="394cb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="394cb-128">-WhatIf</span></span>
<span data-ttu-id="394cb-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="394cb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="394cb-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="394cb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="394cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394cb-131">CommonParameters</span></span>
<span data-ttu-id="394cb-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="394cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394cb-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="394cb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394cb-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="394cb-134">INPUTS</span></span>

### <span data-ttu-id="394cb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="394cb-135">System.String</span></span>

## <span data-ttu-id="394cb-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="394cb-136">OUTPUTS</span></span>

### <span data-ttu-id="394cb-137">Microsoft. Azure. Commands. Management. IotHub. modeller. Pssharedaccesstabetureauthorizationrule</span><span class="sxs-lookup"><span data-stu-id="394cb-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="394cb-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="394cb-138">NOTES</span></span>

## <span data-ttu-id="394cb-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="394cb-139">RELATED LINKS</span></span>
