---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: a0b6ddf2a5796c63c3efd20b811a2040db123836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594437"
---
# <span data-ttu-id="0d87f-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0d87f-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="0d87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d87f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d87f-103">Diske erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0d87f-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d87f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d87f-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d87f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d87f-105">DESCRIPTION</span></span>
<span data-ttu-id="0d87f-106">**Revoke-AzureRmDiskAccess** cmdlet 'i diske erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0d87f-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="0d87f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d87f-107">EXAMPLES</span></span>

### <span data-ttu-id="0d87f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0d87f-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="0d87f-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Disk01 ' adındaki diske erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="0d87f-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="0d87f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d87f-110">PARAMETERS</span></span>

### <span data-ttu-id="0d87f-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="0d87f-111">-AsJob</span></span>
<span data-ttu-id="0d87f-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0d87f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d87f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d87f-113">-DefaultProfile</span></span>
<span data-ttu-id="0d87f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d87f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d87f-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0d87f-115">-DiskName</span></span>
<span data-ttu-id="0d87f-116">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d87f-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="0d87f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d87f-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d87f-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d87f-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0d87f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d87f-119">-Confirm</span></span>
<span data-ttu-id="0d87f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d87f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d87f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d87f-121">-WhatIf</span></span>
<span data-ttu-id="0d87f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d87f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d87f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d87f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d87f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d87f-124">CommonParameters</span></span>
<span data-ttu-id="0d87f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d87f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d87f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d87f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d87f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d87f-127">INPUTS</span></span>

### <span data-ttu-id="0d87f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0d87f-128">System.String</span></span>

## <span data-ttu-id="0d87f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d87f-129">OUTPUTS</span></span>

### <span data-ttu-id="0d87f-130">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="0d87f-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0d87f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d87f-131">NOTES</span></span>

## <span data-ttu-id="0d87f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d87f-132">RELATED LINKS</span></span>
