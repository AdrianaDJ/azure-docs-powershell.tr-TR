---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 373647cfc06c36a510a8208424d00087f00e693e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586679"
---
# <span data-ttu-id="26c45-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="26c45-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="26c45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c45-102">SYNOPSIS</span></span>
<span data-ttu-id="26c45-103">Medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26c45-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26c45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26c45-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26c45-105">DESCRIPTION</span></span>
<span data-ttu-id="26c45-106">**Remove-AzureRmMediaService** cmdlet 'i bir medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26c45-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="26c45-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26c45-107">EXAMPLES</span></span>

### <span data-ttu-id="26c45-108">Örnek 1: medya hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="26c45-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="26c45-109">Bu komut, ResourceGroup001 adındaki kaynak grubundaki MediaService0011 adındaki medya hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26c45-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="26c45-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26c45-110">PARAMETERS</span></span>

### <span data-ttu-id="26c45-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26c45-111">-AccountName</span></span>
<span data-ttu-id="26c45-112">Bu cmdlet 'in kaldırdığı medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26c45-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c45-113">-DefaultProfile</span></span>
<span data-ttu-id="26c45-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="26c45-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26c45-115">-Force</span><span class="sxs-lookup"><span data-stu-id="26c45-115">-Force</span></span>
<span data-ttu-id="26c45-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="26c45-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c45-117">-ResourceGroupName</span></span>
<span data-ttu-id="26c45-118">Medya hizmeti 'ni içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="26c45-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="26c45-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="26c45-119">-Confirm</span></span>
<span data-ttu-id="26c45-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26c45-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c45-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c45-121">-WhatIf</span></span>
<span data-ttu-id="26c45-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26c45-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c45-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26c45-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c45-124">CommonParameters</span></span>
<span data-ttu-id="26c45-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26c45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c45-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26c45-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c45-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26c45-127">INPUTS</span></span>

### <span data-ttu-id="26c45-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="26c45-128">None</span></span>
<span data-ttu-id="26c45-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="26c45-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26c45-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26c45-130">OUTPUTS</span></span>

### <span data-ttu-id="26c45-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26c45-131">System.Boolean</span></span>

## <span data-ttu-id="26c45-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26c45-132">NOTES</span></span>

## <span data-ttu-id="26c45-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26c45-133">RELATED LINKS</span></span>

[<span data-ttu-id="26c45-134">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="26c45-134">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="26c45-135">Yeni-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="26c45-135">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="26c45-136">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="26c45-136">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


