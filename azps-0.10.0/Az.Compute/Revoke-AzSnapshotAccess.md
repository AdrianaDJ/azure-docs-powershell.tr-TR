---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 4c22f8cf7ded27083ad6f1ddbd5994241d542c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936883"
---
# <span data-ttu-id="4c25e-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4c25e-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="4c25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c25e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c25e-103">Anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4c25e-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="4c25e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c25e-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c25e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c25e-105">DESCRIPTION</span></span>
<span data-ttu-id="4c25e-106">**Revoke-AzSnapshotAccess** cmdlet 'i anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="4c25e-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="4c25e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c25e-107">EXAMPLES</span></span>

### <span data-ttu-id="4c25e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c25e-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="4c25e-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="4c25e-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="4c25e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c25e-110">PARAMETERS</span></span>

### <span data-ttu-id="4c25e-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4c25e-111">-AsJob</span></span>
<span data-ttu-id="4c25e-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4c25e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c25e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c25e-113">-DefaultProfile</span></span>
<span data-ttu-id="4c25e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c25e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c25e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c25e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c25e-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c25e-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4c25e-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4c25e-117">-SnapshotName</span></span>
<span data-ttu-id="4c25e-118">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c25e-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4c25e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c25e-119">-Confirm</span></span>
<span data-ttu-id="4c25e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c25e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c25e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c25e-121">-WhatIf</span></span>
<span data-ttu-id="4c25e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c25e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c25e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c25e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c25e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c25e-124">CommonParameters</span></span>
<span data-ttu-id="4c25e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c25e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c25e-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c25e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c25e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c25e-127">INPUTS</span></span>

### <span data-ttu-id="4c25e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4c25e-128">System.String</span></span>

## <span data-ttu-id="4c25e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c25e-129">OUTPUTS</span></span>

### <span data-ttu-id="4c25e-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="4c25e-130">System.Object</span></span>

## <span data-ttu-id="4c25e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c25e-131">NOTES</span></span>

## <span data-ttu-id="4c25e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c25e-132">RELATED LINKS</span></span>

