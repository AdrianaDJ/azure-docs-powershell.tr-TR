---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 5d496d4d79c13208c3c48a9d01bfe010ef64c244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761286"
---
# <span data-ttu-id="25ddf-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="25ddf-101">Remove-AzImage</span></span>

## <span data-ttu-id="25ddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="25ddf-103">Bir resmi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25ddf-103">Removes an image.</span></span>

## <span data-ttu-id="25ddf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25ddf-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25ddf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25ddf-105">DESCRIPTION</span></span>
<span data-ttu-id="25ddf-106">**Remove-AzImage** cmdlet 'i bir resmi kaldırır..</span><span class="sxs-lookup"><span data-stu-id="25ddf-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="25ddf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25ddf-107">EXAMPLES</span></span>

### <span data-ttu-id="25ddf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25ddf-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="25ddf-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Image01 ' adındaki resmi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="25ddf-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="25ddf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25ddf-110">PARAMETERS</span></span>

### <span data-ttu-id="25ddf-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="25ddf-111">-AsJob</span></span>
<span data-ttu-id="25ddf-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="25ddf-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="25ddf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ddf-113">-DefaultProfile</span></span>
<span data-ttu-id="25ddf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25ddf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25ddf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="25ddf-115">-Force</span></span>
<span data-ttu-id="25ddf-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="25ddf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25ddf-117">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="25ddf-117">-ImageName</span></span>
<span data-ttu-id="25ddf-118">Bir resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25ddf-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="25ddf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ddf-119">-ResourceGroupName</span></span>
<span data-ttu-id="25ddf-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="25ddf-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25ddf-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="25ddf-121">-Confirm</span></span>
<span data-ttu-id="25ddf-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25ddf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ddf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ddf-123">-WhatIf</span></span>
<span data-ttu-id="25ddf-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25ddf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25ddf-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25ddf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ddf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ddf-126">CommonParameters</span></span>
<span data-ttu-id="25ddf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25ddf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ddf-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25ddf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ddf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25ddf-129">INPUTS</span></span>

### <span data-ttu-id="25ddf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25ddf-130">System.String</span></span>

## <span data-ttu-id="25ddf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25ddf-131">OUTPUTS</span></span>

### <span data-ttu-id="25ddf-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="25ddf-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="25ddf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25ddf-133">NOTES</span></span>

## <span data-ttu-id="25ddf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25ddf-134">RELATED LINKS</span></span>
