---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 47d10b02cbe019571a94ffcc1384340daff15c31
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938623"
---
# <span data-ttu-id="7e596-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7e596-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="7e596-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e596-102">SYNOPSIS</span></span>
<span data-ttu-id="7e596-103">Toplu hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e596-103">Removes a Batch account.</span></span>

## <span data-ttu-id="7e596-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e596-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e596-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e596-105">DESCRIPTION</span></span>
<span data-ttu-id="7e596-106">**Remove-AzBatchAccount** cmdlet 'ı bir Azure toplu hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e596-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="7e596-107">*Force* parametresini belirtmediğiniz sürece, bu cmdlet bir hesabı kaldırmadan önce size sorar.</span><span class="sxs-lookup"><span data-stu-id="7e596-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="7e596-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e596-108">EXAMPLES</span></span>

### <span data-ttu-id="7e596-109">Örnek 1: toplu Iş hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7e596-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="7e596-110">Bu komut, pfuller adlı toplu hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7e596-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="7e596-111">Bu komut, hesabı silmeden önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e596-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="7e596-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e596-112">PARAMETERS</span></span>

### <span data-ttu-id="7e596-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e596-113">-AccountName</span></span>
<span data-ttu-id="7e596-114">Bu cmdlet 'in kaldırdığı toplu hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e596-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e596-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e596-115">-DefaultProfile</span></span>
<span data-ttu-id="7e596-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e596-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e596-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7e596-117">-Force</span></span>
<span data-ttu-id="7e596-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7e596-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e596-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e596-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e596-120">Bu cmdlet 'in kaldırdığı hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e596-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e596-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e596-121">-Confirm</span></span>
<span data-ttu-id="7e596-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e596-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e596-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e596-123">-WhatIf</span></span>
<span data-ttu-id="7e596-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e596-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e596-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e596-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e596-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e596-126">CommonParameters</span></span>
<span data-ttu-id="7e596-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e596-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e596-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e596-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e596-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e596-129">INPUTS</span></span>

### <span data-ttu-id="7e596-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e596-130">System.String</span></span>

## <span data-ttu-id="7e596-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e596-131">OUTPUTS</span></span>

### <span data-ttu-id="7e596-132">System. void</span><span class="sxs-lookup"><span data-stu-id="7e596-132">System.Void</span></span>

## <span data-ttu-id="7e596-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e596-133">NOTES</span></span>

## <span data-ttu-id="7e596-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e596-134">RELATED LINKS</span></span>

[<span data-ttu-id="7e596-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7e596-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="7e596-136">Yeni-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7e596-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="7e596-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7e596-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="7e596-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="7e596-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

