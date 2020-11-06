---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 30029a6fbd14a7e94ffe60f058405a2907b1cb53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588538"
---
# <span data-ttu-id="b61fb-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b61fb-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="b61fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b61fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b61fb-103">Diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b61fb-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b61fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b61fb-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b61fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b61fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b61fb-106">**Remove-Azurermdısk** cmdlet 'i diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b61fb-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="b61fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b61fb-107">EXAMPLES</span></span>

### <span data-ttu-id="b61fb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b61fb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="b61fb-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Disk01 ' adlı diski kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b61fb-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b61fb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b61fb-110">PARAMETERS</span></span>

### <span data-ttu-id="b61fb-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="b61fb-111">-AsJob</span></span>
<span data-ttu-id="b61fb-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b61fb-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b61fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61fb-113">-DefaultProfile</span></span>
<span data-ttu-id="b61fb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b61fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61fb-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b61fb-115">-DiskName</span></span>
<span data-ttu-id="b61fb-116">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b61fb-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61fb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b61fb-117">-Force</span></span>
<span data-ttu-id="b61fb-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b61fb-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b61fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="b61fb-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b61fb-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61fb-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="b61fb-121">-Confirm</span></span>
<span data-ttu-id="b61fb-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b61fb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b61fb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b61fb-123">-WhatIf</span></span>
<span data-ttu-id="b61fb-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b61fb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b61fb-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b61fb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b61fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61fb-126">CommonParameters</span></span>
<span data-ttu-id="b61fb-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b61fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61fb-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61fb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61fb-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b61fb-129">INPUTS</span></span>

### <span data-ttu-id="b61fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b61fb-130">System.String</span></span>

## <span data-ttu-id="b61fb-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b61fb-131">OUTPUTS</span></span>

### <span data-ttu-id="b61fb-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="b61fb-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b61fb-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b61fb-133">NOTES</span></span>

## <span data-ttu-id="b61fb-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b61fb-134">RELATED LINKS</span></span>
