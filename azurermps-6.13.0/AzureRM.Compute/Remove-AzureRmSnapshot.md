---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: edd2d89cfe0488021ef62780ade80cb2b98437c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587268"
---
# <span data-ttu-id="4bcaf-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bcaf-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="4bcaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcaf-103">Anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bcaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bcaf-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcaf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bcaf-105">DESCRIPTION</span></span>
<span data-ttu-id="4bcaf-106">**Remove-AzureRmSnapshot** cmdlet 'ini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="4bcaf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bcaf-107">EXAMPLES</span></span>

### <span data-ttu-id="4bcaf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bcaf-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="4bcaf-109">Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4bcaf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bcaf-110">PARAMETERS</span></span>

### <span data-ttu-id="4bcaf-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4bcaf-111">-AsJob</span></span>
<span data-ttu-id="4bcaf-112">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4bcaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcaf-113">-DefaultProfile</span></span>
<span data-ttu-id="4bcaf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bcaf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4bcaf-115">-Force</span></span>
<span data-ttu-id="4bcaf-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bcaf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcaf-117">-ResourceGroupName</span></span>
<span data-ttu-id="4bcaf-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4bcaf-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4bcaf-119">-SnapshotName</span></span>
<span data-ttu-id="4bcaf-120">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4bcaf-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bcaf-121">-Confirm</span></span>
<span data-ttu-id="4bcaf-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcaf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcaf-123">-WhatIf</span></span>
<span data-ttu-id="4bcaf-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcaf-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcaf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcaf-126">CommonParameters</span></span>
<span data-ttu-id="4bcaf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bcaf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcaf-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcaf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcaf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bcaf-129">INPUTS</span></span>

### <span data-ttu-id="4bcaf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4bcaf-130">System.String</span></span>

## <span data-ttu-id="4bcaf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bcaf-131">OUTPUTS</span></span>

### <span data-ttu-id="4bcaf-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="4bcaf-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4bcaf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bcaf-133">NOTES</span></span>

## <span data-ttu-id="4bcaf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bcaf-134">RELATED LINKS</span></span>
