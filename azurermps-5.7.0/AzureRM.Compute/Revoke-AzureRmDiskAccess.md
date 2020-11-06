---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594118"
---
# <span data-ttu-id="046d8-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="046d8-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="046d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046d8-102">SYNOPSIS</span></span>
<span data-ttu-id="046d8-103">Diske erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="046d8-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="046d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="046d8-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="046d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="046d8-105">DESCRIPTION</span></span>
<span data-ttu-id="046d8-106">**Revoke-AzureRmDiskAccess** cmdlet 'i diske erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="046d8-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="046d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="046d8-107">EXAMPLES</span></span>

### <span data-ttu-id="046d8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="046d8-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="046d8-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Disk01 ' adındaki diske erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="046d8-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="046d8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="046d8-110">PARAMETERS</span></span>

### <span data-ttu-id="046d8-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="046d8-111">-DiskName</span></span>
<span data-ttu-id="046d8-112">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="046d8-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="046d8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d8-113">-ResourceGroupName</span></span>
<span data-ttu-id="046d8-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="046d8-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="046d8-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="046d8-115">-Confirm</span></span>
<span data-ttu-id="046d8-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="046d8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046d8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046d8-117">-WhatIf</span></span>
<span data-ttu-id="046d8-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="046d8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="046d8-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="046d8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046d8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046d8-120">CommonParameters</span></span>
<span data-ttu-id="046d8-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="046d8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046d8-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046d8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046d8-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="046d8-123">INPUTS</span></span>

### <span data-ttu-id="046d8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="046d8-124">System.String</span></span>

## <span data-ttu-id="046d8-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="046d8-125">OUTPUTS</span></span>

### <span data-ttu-id="046d8-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="046d8-126">System.Object</span></span>

## <span data-ttu-id="046d8-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="046d8-127">NOTES</span></span>

## <span data-ttu-id="046d8-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="046d8-128">RELATED LINKS</span></span>

