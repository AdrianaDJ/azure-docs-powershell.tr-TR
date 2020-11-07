---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 232d6ea05c23ee5023194cca84bd9e5f6857aa20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917399"
---
# <span data-ttu-id="53c85-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="53c85-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="53c85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c85-102">SYNOPSIS</span></span>
<span data-ttu-id="53c85-103">Diske erişim verir.</span><span class="sxs-lookup"><span data-stu-id="53c85-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="53c85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53c85-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53c85-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="53c85-105">DESCRIPTION</span></span>
<span data-ttu-id="53c85-106">**Grant-AzDiskAccess** cmdlet 'ine bir diske erişim veriyor.</span><span class="sxs-lookup"><span data-stu-id="53c85-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="53c85-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53c85-107">EXAMPLES</span></span>

### <span data-ttu-id="53c85-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="53c85-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="53c85-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Disk01 ' adındaki diske ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="53c85-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="53c85-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53c85-110">PARAMETERS</span></span>

### <span data-ttu-id="53c85-111">-Access</span><span class="sxs-lookup"><span data-stu-id="53c85-111">-Access</span></span>
<span data-ttu-id="53c85-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="53c85-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="53c85-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="53c85-113">-AsJob</span></span>
<span data-ttu-id="53c85-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="53c85-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53c85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c85-115">-DefaultProfile</span></span>
<span data-ttu-id="53c85-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53c85-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53c85-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="53c85-117">-DiskName</span></span>
<span data-ttu-id="53c85-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53c85-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="53c85-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="53c85-119">-DurationInSecond</span></span>
<span data-ttu-id="53c85-120">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="53c85-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53c85-121">-ResourceGroupName</span></span>
<span data-ttu-id="53c85-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53c85-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53c85-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="53c85-123">-Confirm</span></span>
<span data-ttu-id="53c85-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="53c85-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c85-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c85-125">-WhatIf</span></span>
<span data-ttu-id="53c85-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="53c85-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53c85-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="53c85-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c85-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c85-128">CommonParameters</span></span>
<span data-ttu-id="53c85-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53c85-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c85-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c85-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c85-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53c85-131">INPUTS</span></span>

### <span data-ttu-id="53c85-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53c85-132">System.String</span></span>

## <span data-ttu-id="53c85-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53c85-133">OUTPUTS</span></span>

### <span data-ttu-id="53c85-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="53c85-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="53c85-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53c85-135">NOTES</span></span>

## <span data-ttu-id="53c85-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53c85-136">RELATED LINKS</span></span>
