---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: e9d117e9e81ee1189031b9e1f2f0a4094e9b9fcf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915747"
---
# <span data-ttu-id="de4d6-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="de4d6-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="de4d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="de4d6-103">Medya hizmetiyle ilişkili REST uç noktasına erişmek için kullanılan anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4d6-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="de4d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de4d6-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de4d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="de4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="de4d6-106">**Set-AzMediaServiceKey** cmdlet 'i, medya hizmetiyle Ilişkili representational durum aktarma (REST) uç noktasına erişmek için kullanılan bir anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4d6-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="de4d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="de4d6-108">Örnek 1: medya hizmetine erişmek için kullanılan birincil anahtarı yeniden üret</span><span class="sxs-lookup"><span data-stu-id="de4d6-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="de4d6-109">Bu komut, ResourceGroup004 adındaki kaynak grubuna ait MediaService001 adındaki medya hizmeti için birincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4d6-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="de4d6-110">Örnek 2: medya hizmetine erişmek için kullanılan ikincil anahtarı yeniden oluşturur</span><span class="sxs-lookup"><span data-stu-id="de4d6-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="de4d6-111">Bu komut, Resourcegroup123 adındaki kaynak grubuna ait MediaService002 adındaki medya hizmeti için ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4d6-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="de4d6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de4d6-112">PARAMETERS</span></span>

### <span data-ttu-id="de4d6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de4d6-113">-AccountName</span></span>
<span data-ttu-id="de4d6-114">Bu cmdlet 'in yeniden kullandığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4d6-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="de4d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4d6-115">-DefaultProfile</span></span>
<span data-ttu-id="de4d6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="de4d6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de4d6-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="de4d6-117">-KeyType</span></span>
<span data-ttu-id="de4d6-118">Medya hizmetinin anahtar türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4d6-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="de4d6-119">Bu parametre için kabul edilebilir değerler: birincil veya Ikincil.</span><span class="sxs-lookup"><span data-stu-id="de4d6-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="de4d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="de4d6-121">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4d6-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="de4d6-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="de4d6-122">-Confirm</span></span>
<span data-ttu-id="de4d6-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de4d6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de4d6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4d6-124">-WhatIf</span></span>
<span data-ttu-id="de4d6-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de4d6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de4d6-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de4d6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de4d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4d6-127">CommonParameters</span></span>
<span data-ttu-id="de4d6-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de4d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4d6-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de4d6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4d6-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de4d6-130">INPUTS</span></span>

### <span data-ttu-id="de4d6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="de4d6-131">System.String</span></span>

## <span data-ttu-id="de4d6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de4d6-132">OUTPUTS</span></span>

### <span data-ttu-id="de4d6-133">Microsoft. Azure. Commands. Media. modeller. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="de4d6-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="de4d6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de4d6-134">NOTES</span></span>

## <span data-ttu-id="de4d6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de4d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="de4d6-136">Get-AzMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="de4d6-136">Get-AzMediaServiceKeys</span></span>](./Get-AzMediaServiceKeys.md)

