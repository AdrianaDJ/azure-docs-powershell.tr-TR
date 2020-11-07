---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: da9fa6503e76d9af8efbdff84ebbcdd501d8232d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935219"
---
# <span data-ttu-id="c1395-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="c1395-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="c1395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1395-102">SYNOPSIS</span></span>
<span data-ttu-id="c1395-103">Bir makineden tüm AzureRm modüllerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1395-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="c1395-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1395-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1395-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1395-105">DESCRIPTION</span></span>
<span data-ttu-id="c1395-106">Bir makineden tüm AzureRm modüllerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c1395-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="c1395-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1395-107">EXAMPLES</span></span>

### <span data-ttu-id="c1395-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c1395-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="c1395-109">Bu komut çalıştırıldığında, cmdlet 'in çalıştırıldığı PowerShell sürümü için makineden tüm AzureRm modülleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c1395-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="c1395-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1395-110">PARAMETERS</span></span>

### <span data-ttu-id="c1395-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1395-111">-DefaultProfile</span></span>
<span data-ttu-id="c1395-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1395-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1395-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c1395-113">-PassThru</span></span>
<span data-ttu-id="c1395-114">Belirtilmişse kaldırılan modüllerin dönüş listesi.</span><span class="sxs-lookup"><span data-stu-id="c1395-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="c1395-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1395-115">-Confirm</span></span>
<span data-ttu-id="c1395-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1395-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1395-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1395-117">-WhatIf</span></span>
<span data-ttu-id="c1395-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1395-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1395-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1395-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1395-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1395-120">CommonParameters</span></span>
<span data-ttu-id="c1395-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1395-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1395-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1395-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1395-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1395-123">INPUTS</span></span>

### <span data-ttu-id="c1395-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c1395-124">None</span></span>

## <span data-ttu-id="c1395-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1395-125">OUTPUTS</span></span>

### <span data-ttu-id="c1395-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c1395-126">System.String</span></span>

## <span data-ttu-id="c1395-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1395-127">NOTES</span></span>

## <span data-ttu-id="c1395-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1395-128">RELATED LINKS</span></span>
