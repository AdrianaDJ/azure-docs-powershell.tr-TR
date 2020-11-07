---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939607"
---
# <span data-ttu-id="80f3c-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="80f3c-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="80f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="80f3c-103">Diske erişim verir.</span><span class="sxs-lookup"><span data-stu-id="80f3c-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80f3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80f3c-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80f3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="80f3c-106">**Grant-AzureRmDiskAccess** cmdlet 'ine bir diske erişim veriyor.</span><span class="sxs-lookup"><span data-stu-id="80f3c-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="80f3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="80f3c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="80f3c-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="80f3c-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Disk01 ' adındaki diske ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="80f3c-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="80f3c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80f3c-110">PARAMETERS</span></span>

### <span data-ttu-id="80f3c-111">-Access</span><span class="sxs-lookup"><span data-stu-id="80f3c-111">-Access</span></span>
<span data-ttu-id="80f3c-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="80f3c-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f3c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="80f3c-113">-AsJob</span></span>
<span data-ttu-id="80f3c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="80f3c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80f3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f3c-115">-DefaultProfile</span></span>
<span data-ttu-id="80f3c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80f3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f3c-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="80f3c-117">-DiskName</span></span>
<span data-ttu-id="80f3c-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80f3c-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="80f3c-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="80f3c-119">-DurationInSecond</span></span>
<span data-ttu-id="80f3c-120">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="80f3c-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="80f3c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f3c-121">-ResourceGroupName</span></span>
<span data-ttu-id="80f3c-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80f3c-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="80f3c-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="80f3c-123">-Confirm</span></span>
<span data-ttu-id="80f3c-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="80f3c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f3c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f3c-125">-WhatIf</span></span>
<span data-ttu-id="80f3c-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80f3c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80f3c-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="80f3c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f3c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f3c-128">CommonParameters</span></span>
<span data-ttu-id="80f3c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80f3c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f3c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80f3c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f3c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80f3c-131">INPUTS</span></span>

### <span data-ttu-id="80f3c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="80f3c-132">System.String</span></span>

## <span data-ttu-id="80f3c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80f3c-133">OUTPUTS</span></span>

### <span data-ttu-id="80f3c-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="80f3c-134">System.Object</span></span>

## <span data-ttu-id="80f3c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80f3c-135">NOTES</span></span>

## <span data-ttu-id="80f3c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80f3c-136">RELATED LINKS</span></span>

