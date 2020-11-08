---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097465"
---
# <span data-ttu-id="d21ee-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="d21ee-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="d21ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d21ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d21ee-103">Bir makineden tüm AzureRm modüllerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d21ee-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="d21ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d21ee-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d21ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d21ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d21ee-106">Bir makineden tüm AzureRm modüllerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d21ee-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="d21ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d21ee-107">EXAMPLES</span></span>

### <span data-ttu-id="d21ee-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d21ee-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="d21ee-109">Bu komut çalıştırıldığında, cmdlet 'in çalıştırıldığı PowerShell sürümü için makineden tüm AzureRm modülleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d21ee-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="d21ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d21ee-110">PARAMETERS</span></span>

### <span data-ttu-id="d21ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d21ee-111">-DefaultProfile</span></span>
<span data-ttu-id="d21ee-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d21ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d21ee-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d21ee-113">-PassThru</span></span>
<span data-ttu-id="d21ee-114">Belirtilmişse kaldırılan modüllerin dönüş listesi.</span><span class="sxs-lookup"><span data-stu-id="d21ee-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="d21ee-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d21ee-115">-Confirm</span></span>
<span data-ttu-id="d21ee-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d21ee-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d21ee-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d21ee-117">-WhatIf</span></span>
<span data-ttu-id="d21ee-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d21ee-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d21ee-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d21ee-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d21ee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21ee-120">CommonParameters</span></span>
<span data-ttu-id="d21ee-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d21ee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21ee-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d21ee-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21ee-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d21ee-123">INPUTS</span></span>

### <span data-ttu-id="d21ee-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d21ee-124">None</span></span>

## <span data-ttu-id="d21ee-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d21ee-125">OUTPUTS</span></span>

### <span data-ttu-id="d21ee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d21ee-126">System.String</span></span>

## <span data-ttu-id="d21ee-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d21ee-127">NOTES</span></span>

## <span data-ttu-id="d21ee-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d21ee-128">RELATED LINKS</span></span>