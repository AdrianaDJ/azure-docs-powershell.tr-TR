---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: b60abc403beea938e24ffaa59e634a36611d150b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590369"
---
# <span data-ttu-id="b5c2a-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b5c2a-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="b5c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c2a-103">Anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5c2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5c2a-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5c2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c2a-106">**Grant-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişim verir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="b5c2a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c2a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5c2a-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="b5c2a-109">60 saniye için ' ResourceGroup01 ' adındaki kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye ' Read ' erişimi verin.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="b5c2a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5c2a-110">PARAMETERS</span></span>

### <span data-ttu-id="b5c2a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="b5c2a-111">-Access</span></span>
<span data-ttu-id="b5c2a-112">Erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c2a-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="b5c2a-113">-AsJob</span></span>
<span data-ttu-id="b5c2a-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b5c2a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5c2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c2a-115">-DefaultProfile</span></span>
<span data-ttu-id="b5c2a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5c2a-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="b5c2a-117">-DurationInSecond</span></span>
<span data-ttu-id="b5c2a-118">Erişim süresini saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5c2a-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b5c2a-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b5c2a-121">-SnapshotName</span></span>
<span data-ttu-id="b5c2a-122">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b5c2a-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5c2a-123">-Confirm</span></span>
<span data-ttu-id="b5c2a-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c2a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c2a-125">-WhatIf</span></span>
<span data-ttu-id="b5c2a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5c2a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c2a-128">CommonParameters</span></span>
<span data-ttu-id="b5c2a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5c2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c2a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c2a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c2a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5c2a-131">INPUTS</span></span>

### <span data-ttu-id="b5c2a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c2a-132">System.String</span></span>

## <span data-ttu-id="b5c2a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5c2a-133">OUTPUTS</span></span>

### <span data-ttu-id="b5c2a-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="b5c2a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="b5c2a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5c2a-135">NOTES</span></span>

## <span data-ttu-id="b5c2a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5c2a-136">RELATED LINKS</span></span>
