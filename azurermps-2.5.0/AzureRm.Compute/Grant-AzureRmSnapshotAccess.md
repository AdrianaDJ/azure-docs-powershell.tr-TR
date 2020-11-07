---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939606"
---
# <span data-ttu-id="c9830-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c9830-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="c9830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9830-102">SYNOPSIS</span></span>
<span data-ttu-id="c9830-103">Anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="c9830-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9830-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9830-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9830-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9830-105">DESCRIPTION</span></span>
<span data-ttu-id="c9830-106">**Grant-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="c9830-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="c9830-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9830-107">EXAMPLES</span></span>

### <span data-ttu-id="c9830-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9830-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="c9830-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="c9830-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="c9830-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9830-110">PARAMETERS</span></span>

### <span data-ttu-id="c9830-111">-Access</span><span class="sxs-lookup"><span data-stu-id="c9830-111">-Access</span></span>
<span data-ttu-id="c9830-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9830-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="c9830-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="c9830-113">-AsJob</span></span>
<span data-ttu-id="c9830-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c9830-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9830-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9830-115">-DefaultProfile</span></span>
<span data-ttu-id="c9830-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9830-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9830-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="c9830-117">-DurationInSecond</span></span>
<span data-ttu-id="c9830-118">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9830-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="c9830-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9830-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9830-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9830-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c9830-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c9830-121">-SnapshotName</span></span>
<span data-ttu-id="c9830-122">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9830-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c9830-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9830-123">-Confirm</span></span>
<span data-ttu-id="c9830-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9830-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9830-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9830-125">-WhatIf</span></span>
<span data-ttu-id="c9830-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9830-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9830-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9830-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9830-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9830-128">CommonParameters</span></span>
<span data-ttu-id="c9830-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9830-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9830-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9830-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9830-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9830-131">INPUTS</span></span>

### <span data-ttu-id="c9830-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c9830-132">System.String</span></span>

## <span data-ttu-id="c9830-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9830-133">OUTPUTS</span></span>

### <span data-ttu-id="c9830-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="c9830-134">System.Object</span></span>

## <span data-ttu-id="c9830-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9830-135">NOTES</span></span>

## <span data-ttu-id="c9830-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9830-136">RELATED LINKS</span></span>

