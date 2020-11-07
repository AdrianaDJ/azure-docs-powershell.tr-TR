---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 46cbb87d54d1eb80857d3d0fbc786cb8296f4ac0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752809"
---
# <span data-ttu-id="f7893-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="f7893-101">Remove-AzDisk</span></span>

## <span data-ttu-id="f7893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7893-102">SYNOPSIS</span></span>
<span data-ttu-id="f7893-103">Diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f7893-103">Removes a disk.</span></span>

## <span data-ttu-id="f7893-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7893-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7893-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7893-105">DESCRIPTION</span></span>
<span data-ttu-id="f7893-106">**Remove-Azdısk** cmdlet 'i diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f7893-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="f7893-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7893-107">EXAMPLES</span></span>

### <span data-ttu-id="f7893-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f7893-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="f7893-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f7893-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f7893-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7893-110">PARAMETERS</span></span>

### <span data-ttu-id="f7893-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f7893-111">-AsJob</span></span>
<span data-ttu-id="f7893-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="f7893-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7893-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7893-113">-DefaultProfile</span></span>
<span data-ttu-id="f7893-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7893-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7893-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f7893-115">-DiskName</span></span>
<span data-ttu-id="f7893-116">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7893-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7893-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f7893-117">-Force</span></span>
<span data-ttu-id="f7893-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f7893-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7893-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7893-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7893-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7893-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f7893-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7893-121">-Confirm</span></span>
<span data-ttu-id="f7893-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7893-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7893-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7893-123">-WhatIf</span></span>
<span data-ttu-id="f7893-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7893-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7893-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7893-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7893-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7893-126">CommonParameters</span></span>
<span data-ttu-id="f7893-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7893-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7893-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f7893-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7893-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7893-129">INPUTS</span></span>

### <span data-ttu-id="f7893-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7893-130">System.String</span></span>

## <span data-ttu-id="f7893-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7893-131">OUTPUTS</span></span>

### <span data-ttu-id="f7893-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="f7893-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f7893-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7893-133">NOTES</span></span>

## <span data-ttu-id="f7893-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7893-134">RELATED LINKS</span></span>
