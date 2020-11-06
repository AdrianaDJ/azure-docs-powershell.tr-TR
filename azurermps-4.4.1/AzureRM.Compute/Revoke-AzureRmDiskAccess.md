---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586949"
---
# <span data-ttu-id="31ec5-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="31ec5-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="31ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="31ec5-103">Diske erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="31ec5-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ec5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31ec5-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ec5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="31ec5-106">**Revoke-AzureRmDiskAccess** cmdlet 'i diske erişimi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="31ec5-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="31ec5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="31ec5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31ec5-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="31ec5-109">' ResourceGroup01 ' adlı kaynak grubundaki ' Disk01 ' adındaki diske erişimi iptal etme</span><span class="sxs-lookup"><span data-stu-id="31ec5-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="31ec5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="31ec5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ec5-111">-DefaultProfile</span></span>
<span data-ttu-id="31ec5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31ec5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ec5-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="31ec5-113">-DiskName</span></span>
<span data-ttu-id="31ec5-114">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31ec5-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="31ec5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ec5-115">-ResourceGroupName</span></span>
<span data-ttu-id="31ec5-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31ec5-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="31ec5-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="31ec5-117">-Confirm</span></span>
<span data-ttu-id="31ec5-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31ec5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ec5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ec5-119">-WhatIf</span></span>
<span data-ttu-id="31ec5-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31ec5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31ec5-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31ec5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ec5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ec5-122">CommonParameters</span></span>
<span data-ttu-id="31ec5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31ec5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ec5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ec5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ec5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31ec5-125">INPUTS</span></span>

### <span data-ttu-id="31ec5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="31ec5-126">System.String</span></span>

## <span data-ttu-id="31ec5-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31ec5-127">OUTPUTS</span></span>

### <span data-ttu-id="31ec5-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="31ec5-128">System.Object</span></span>

## <span data-ttu-id="31ec5-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31ec5-129">NOTES</span></span>

## <span data-ttu-id="31ec5-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31ec5-130">RELATED LINKS</span></span>

