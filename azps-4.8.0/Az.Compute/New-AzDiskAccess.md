---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268596"
---
# <span data-ttu-id="57f22-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="57f22-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="57f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f22-102">SYNOPSIS</span></span>
<span data-ttu-id="57f22-103">Disk erişim kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="57f22-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="57f22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57f22-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57f22-105">DESCRIPTION</span></span>
<span data-ttu-id="57f22-106">**Yeni-Azdıskaccess** cmdlet 'ı disk erişim kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="57f22-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="57f22-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57f22-107">EXAMPLES</span></span>

### <span data-ttu-id="57f22-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57f22-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="57f22-109">Bu komut, verilen özelliklere sahip bir disk erişimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="57f22-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="57f22-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57f22-110">PARAMETERS</span></span>

### <span data-ttu-id="57f22-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="57f22-111">-AsJob</span></span>
<span data-ttu-id="57f22-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="57f22-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57f22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f22-113">-DefaultProfile</span></span>
<span data-ttu-id="57f22-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57f22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f22-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="57f22-115">-Location</span></span>
<span data-ttu-id="57f22-116">Konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="57f22-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57f22-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="57f22-117">-Name</span></span>
<span data-ttu-id="57f22-118">Disk erişiminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57f22-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f22-119">-ResourceGroupName</span></span>
<span data-ttu-id="57f22-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57f22-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="57f22-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="57f22-121">-Confirm</span></span>
<span data-ttu-id="57f22-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57f22-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f22-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f22-123">-WhatIf</span></span>
<span data-ttu-id="57f22-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57f22-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f22-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57f22-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f22-126">CommonParameters</span></span>
<span data-ttu-id="57f22-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57f22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f22-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57f22-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f22-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57f22-129">INPUTS</span></span>

### <span data-ttu-id="57f22-130">System. String</span><span class="sxs-lookup"><span data-stu-id="57f22-130">System.String</span></span>

## <span data-ttu-id="57f22-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57f22-131">OUTPUTS</span></span>

### <span data-ttu-id="57f22-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDısaccess</span><span class="sxs-lookup"><span data-stu-id="57f22-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="57f22-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57f22-133">NOTES</span></span>

## <span data-ttu-id="57f22-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57f22-134">RELATED LINKS</span></span>
