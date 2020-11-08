---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 9e3a194d1143134b1ba3aa472db61062baf847f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936932"
---
# <span data-ttu-id="976a1-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="976a1-101">Remove-AzDisk</span></span>

## <span data-ttu-id="976a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="976a1-102">SYNOPSIS</span></span>
<span data-ttu-id="976a1-103">Diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="976a1-103">Removes a disk.</span></span>

## <span data-ttu-id="976a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="976a1-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="976a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="976a1-105">DESCRIPTION</span></span>
<span data-ttu-id="976a1-106">**Remove-Azdısk** cmdlet 'i diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="976a1-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="976a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="976a1-107">EXAMPLES</span></span>

### <span data-ttu-id="976a1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="976a1-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="976a1-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="976a1-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="976a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="976a1-110">PARAMETERS</span></span>

### <span data-ttu-id="976a1-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="976a1-111">-AsJob</span></span>
<span data-ttu-id="976a1-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="976a1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="976a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976a1-113">-DefaultProfile</span></span>
<span data-ttu-id="976a1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="976a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="976a1-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="976a1-115">-DiskName</span></span>
<span data-ttu-id="976a1-116">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="976a1-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="976a1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="976a1-117">-Force</span></span>
<span data-ttu-id="976a1-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="976a1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="976a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="976a1-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="976a1-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="976a1-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="976a1-121">-Confirm</span></span>
<span data-ttu-id="976a1-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="976a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976a1-123">-WhatIf</span></span>
<span data-ttu-id="976a1-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="976a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976a1-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="976a1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="976a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976a1-126">CommonParameters</span></span>
<span data-ttu-id="976a1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="976a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976a1-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="976a1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976a1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="976a1-129">INPUTS</span></span>

### <span data-ttu-id="976a1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="976a1-130">System.String</span></span>

## <span data-ttu-id="976a1-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="976a1-131">OUTPUTS</span></span>

### <span data-ttu-id="976a1-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="976a1-132">System.Object</span></span>

## <span data-ttu-id="976a1-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="976a1-133">NOTES</span></span>

## <span data-ttu-id="976a1-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="976a1-134">RELATED LINKS</span></span>
