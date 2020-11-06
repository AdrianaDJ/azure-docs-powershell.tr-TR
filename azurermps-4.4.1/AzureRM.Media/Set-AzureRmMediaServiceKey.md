---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 7b8c1b154a631a911100f4b2b8581ca552e4b565
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593545"
---
# <span data-ttu-id="1d438-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="1d438-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="1d438-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d438-102">SYNOPSIS</span></span>
<span data-ttu-id="1d438-103">Medya hizmetiyle ilişkili REST uç noktasına erişmek için kullanılan anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d438-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d438-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d438-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d438-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d438-105">DESCRIPTION</span></span>
<span data-ttu-id="1d438-106">**Set-AzureRmMediaServiceKey** cmdlet 'i, medya hizmetiyle Ilişkili Representational State Transfer (REST) uç noktasına erişmek için kullanılan bir anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d438-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="1d438-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d438-107">EXAMPLES</span></span>

### <span data-ttu-id="1d438-108">Örnek 1: medya hizmetine erişmek için kullanılan birincil anahtarı yeniden üret</span><span class="sxs-lookup"><span data-stu-id="1d438-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="1d438-109">Bu komut, ResourceGroup004 adındaki kaynak grubuna ait MediaService001 adındaki medya hizmeti için birincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d438-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="1d438-110">Örnek 2: medya hizmetine erişmek için kullanılan ikincil anahtarı yeniden oluşturur</span><span class="sxs-lookup"><span data-stu-id="1d438-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="1d438-111">Bu komut, Resourcegroup123 adındaki kaynak grubuna ait MediaService002 adındaki medya hizmeti için ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d438-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="1d438-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d438-112">PARAMETERS</span></span>

### <span data-ttu-id="1d438-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d438-113">-AccountName</span></span>
<span data-ttu-id="1d438-114">Bu cmdlet 'in yeniden kullandığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d438-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d438-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1d438-115">-KeyType</span></span>
<span data-ttu-id="1d438-116">Medya hizmetinin anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d438-116">Specifies the key type of the media service.</span></span>
<span data-ttu-id="1d438-117">Bu parametre için kabul edilebilir değerler: birincil veya Ikincil.</span><span class="sxs-lookup"><span data-stu-id="1d438-117">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d438-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d438-118">-ResourceGroupName</span></span>
<span data-ttu-id="1d438-119">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d438-119">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1d438-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d438-120">-Confirm</span></span>
<span data-ttu-id="1d438-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d438-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d438-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d438-122">-WhatIf</span></span>
<span data-ttu-id="1d438-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d438-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d438-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d438-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d438-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d438-125">-DefaultProfile</span></span>
<span data-ttu-id="1d438-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d438-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d438-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d438-127">CommonParameters</span></span>
<span data-ttu-id="1d438-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d438-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d438-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d438-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d438-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d438-130">INPUTS</span></span>

## <span data-ttu-id="1d438-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d438-131">OUTPUTS</span></span>

### <span data-ttu-id="1d438-132">Microsoft. Azure. Commands. Media. modeller. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="1d438-132">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="1d438-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d438-133">NOTES</span></span>

## <span data-ttu-id="1d438-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d438-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d438-135">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="1d438-135">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


