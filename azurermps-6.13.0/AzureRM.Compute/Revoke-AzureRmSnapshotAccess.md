---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572886"
---
# <span data-ttu-id="5a789-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5a789-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="5a789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a789-102">SYNOPSIS</span></span>
<span data-ttu-id="5a789-103">Anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="5a789-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a789-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a789-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a789-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a789-105">DESCRIPTION</span></span>
<span data-ttu-id="5a789-106">**Revoke-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="5a789-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="5a789-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a789-107">EXAMPLES</span></span>

### <span data-ttu-id="5a789-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5a789-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="5a789-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="5a789-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="5a789-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a789-110">PARAMETERS</span></span>

### <span data-ttu-id="5a789-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5a789-111">-AsJob</span></span>
<span data-ttu-id="5a789-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5a789-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a789-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a789-113">-DefaultProfile</span></span>
<span data-ttu-id="5a789-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a789-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a789-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a789-115">-ResourceGroupName</span></span>
<span data-ttu-id="5a789-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a789-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5a789-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5a789-117">-SnapshotName</span></span>
<span data-ttu-id="5a789-118">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a789-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5a789-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a789-119">-Confirm</span></span>
<span data-ttu-id="5a789-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a789-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a789-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a789-121">-WhatIf</span></span>
<span data-ttu-id="5a789-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a789-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a789-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a789-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a789-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a789-124">CommonParameters</span></span>
<span data-ttu-id="5a789-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a789-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a789-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a789-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a789-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a789-127">INPUTS</span></span>

### <span data-ttu-id="5a789-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5a789-128">System.String</span></span>

## <span data-ttu-id="5a789-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a789-129">OUTPUTS</span></span>

### <span data-ttu-id="5a789-130">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="5a789-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5a789-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a789-131">NOTES</span></span>

## <span data-ttu-id="5a789-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a789-132">RELATED LINKS</span></span>
