---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 5fe22889443d38e10cff061008c4ed2582825887
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936930"
---
# <span data-ttu-id="1568b-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="1568b-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="1568b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1568b-102">SYNOPSIS</span></span>
<span data-ttu-id="1568b-103">Anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1568b-103">Removes a snapshot.</span></span>

## <span data-ttu-id="1568b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1568b-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1568b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1568b-105">DESCRIPTION</span></span>
<span data-ttu-id="1568b-106">**Remove-AzSnapshot** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1568b-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="1568b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1568b-107">EXAMPLES</span></span>

### <span data-ttu-id="1568b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1568b-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="1568b-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1568b-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1568b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1568b-110">PARAMETERS</span></span>

### <span data-ttu-id="1568b-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1568b-111">-AsJob</span></span>
<span data-ttu-id="1568b-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="1568b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1568b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1568b-113">-DefaultProfile</span></span>
<span data-ttu-id="1568b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1568b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1568b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1568b-115">-Force</span></span>
<span data-ttu-id="1568b-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1568b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1568b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1568b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1568b-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1568b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1568b-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1568b-119">-SnapshotName</span></span>
<span data-ttu-id="1568b-120">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1568b-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1568b-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1568b-121">-Confirm</span></span>
<span data-ttu-id="1568b-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1568b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1568b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1568b-123">-WhatIf</span></span>
<span data-ttu-id="1568b-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1568b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1568b-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1568b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1568b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1568b-126">CommonParameters</span></span>
<span data-ttu-id="1568b-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1568b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1568b-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1568b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1568b-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1568b-129">INPUTS</span></span>

### <span data-ttu-id="1568b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1568b-130">System.String</span></span>

## <span data-ttu-id="1568b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1568b-131">OUTPUTS</span></span>

### <span data-ttu-id="1568b-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="1568b-132">System.Object</span></span>

## <span data-ttu-id="1568b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1568b-133">NOTES</span></span>

## <span data-ttu-id="1568b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1568b-134">RELATED LINKS</span></span>

