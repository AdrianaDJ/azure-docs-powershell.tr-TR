---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: 6d7b41ae7250a294b86333ecf2926a2eda06d3bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762064"
---
# <span data-ttu-id="741ae-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="741ae-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="741ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741ae-102">SYNOPSIS</span></span>
<span data-ttu-id="741ae-103">Anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="741ae-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="741ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="741ae-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="741ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="741ae-105">DESCRIPTION</span></span>
<span data-ttu-id="741ae-106">**Revoke-AzureRmSnapshotAccess** cmdlet 'i anlık görüntüye erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="741ae-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="741ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="741ae-107">EXAMPLES</span></span>

### <span data-ttu-id="741ae-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="741ae-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="741ae-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüye erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="741ae-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="741ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="741ae-110">PARAMETERS</span></span>

### <span data-ttu-id="741ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741ae-111">-DefaultProfile</span></span>
<span data-ttu-id="741ae-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="741ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="741ae-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741ae-113">-ResourceGroupName</span></span>
<span data-ttu-id="741ae-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="741ae-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="741ae-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="741ae-115">-SnapshotName</span></span>
<span data-ttu-id="741ae-116">Anlık görüntünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="741ae-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="741ae-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="741ae-117">-Confirm</span></span>
<span data-ttu-id="741ae-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="741ae-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741ae-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741ae-119">-WhatIf</span></span>
<span data-ttu-id="741ae-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="741ae-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="741ae-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="741ae-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741ae-122">CommonParameters</span></span>
<span data-ttu-id="741ae-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="741ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741ae-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="741ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741ae-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="741ae-125">INPUTS</span></span>

### <span data-ttu-id="741ae-126">System. String</span><span class="sxs-lookup"><span data-stu-id="741ae-126">System.String</span></span>

## <span data-ttu-id="741ae-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="741ae-127">OUTPUTS</span></span>

### <span data-ttu-id="741ae-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="741ae-128">System.Object</span></span>

## <span data-ttu-id="741ae-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="741ae-129">NOTES</span></span>

## <span data-ttu-id="741ae-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="741ae-130">RELATED LINKS</span></span>

