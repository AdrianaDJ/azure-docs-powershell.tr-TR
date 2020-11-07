---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: d2e495b58e68232bf20bd309d06207cd45cd427e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753700"
---
# <span data-ttu-id="9125b-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="9125b-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="9125b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9125b-102">SYNOPSIS</span></span>
<span data-ttu-id="9125b-103">Bir makineden tüm AzureRm modüllerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9125b-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="9125b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9125b-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9125b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9125b-105">DESCRIPTION</span></span>
<span data-ttu-id="9125b-106">Bir makineden tüm AzureRm modüllerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9125b-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="9125b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9125b-107">EXAMPLES</span></span>

### <span data-ttu-id="9125b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9125b-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="9125b-109">Bu komut çalıştırıldığında, cmdlet 'in çalıştırıldığı PowerShell sürümü için makineden tüm AzureRm modülleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="9125b-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="9125b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9125b-110">PARAMETERS</span></span>

### <span data-ttu-id="9125b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9125b-111">-DefaultProfile</span></span>
<span data-ttu-id="9125b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9125b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9125b-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9125b-113">-PassThru</span></span>
<span data-ttu-id="9125b-114">Belirtilmişse kaldırılan modüllerin dönüş listesi.</span><span class="sxs-lookup"><span data-stu-id="9125b-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="9125b-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="9125b-115">-Confirm</span></span>
<span data-ttu-id="9125b-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9125b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9125b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9125b-117">-WhatIf</span></span>
<span data-ttu-id="9125b-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9125b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9125b-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9125b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9125b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9125b-120">CommonParameters</span></span>
<span data-ttu-id="9125b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9125b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9125b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9125b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9125b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9125b-123">INPUTS</span></span>

### <span data-ttu-id="9125b-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9125b-124">None</span></span>

## <span data-ttu-id="9125b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9125b-125">OUTPUTS</span></span>

### <span data-ttu-id="9125b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9125b-126">System.String</span></span>

## <span data-ttu-id="9125b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9125b-127">NOTES</span></span>

## <span data-ttu-id="9125b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9125b-128">RELATED LINKS</span></span>
