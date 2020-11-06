---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587618"
---
# <span data-ttu-id="3490a-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3490a-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="3490a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3490a-102">SYNOPSIS</span></span>
<span data-ttu-id="3490a-103">Diske erişim verir.</span><span class="sxs-lookup"><span data-stu-id="3490a-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3490a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3490a-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3490a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3490a-105">DESCRIPTION</span></span>
<span data-ttu-id="3490a-106">**Grant-AzureRmDiskAccess** cmdlet 'ine bir diske erişim veriyor.</span><span class="sxs-lookup"><span data-stu-id="3490a-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="3490a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3490a-107">EXAMPLES</span></span>

### <span data-ttu-id="3490a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3490a-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="3490a-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Disk01 ' adındaki diske ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="3490a-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="3490a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3490a-110">PARAMETERS</span></span>

### <span data-ttu-id="3490a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="3490a-111">-Access</span></span>
<span data-ttu-id="3490a-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3490a-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3490a-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3490a-113">-DiskName</span></span>
<span data-ttu-id="3490a-114">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3490a-114">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3490a-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="3490a-115">-DurationInSecond</span></span>
<span data-ttu-id="3490a-116">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="3490a-116">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3490a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3490a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3490a-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3490a-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3490a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3490a-119">-Confirm</span></span>
<span data-ttu-id="3490a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3490a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3490a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3490a-121">-WhatIf</span></span>
<span data-ttu-id="3490a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3490a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3490a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3490a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3490a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3490a-124">CommonParameters</span></span>
<span data-ttu-id="3490a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3490a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3490a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3490a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3490a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3490a-127">INPUTS</span></span>

### <span data-ttu-id="3490a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3490a-128">System.String</span></span>

## <span data-ttu-id="3490a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3490a-129">OUTPUTS</span></span>

### <span data-ttu-id="3490a-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="3490a-130">System.Object</span></span>

## <span data-ttu-id="3490a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3490a-131">NOTES</span></span>

## <span data-ttu-id="3490a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3490a-132">RELATED LINKS</span></span>

