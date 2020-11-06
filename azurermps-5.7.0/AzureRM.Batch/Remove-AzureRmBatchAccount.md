---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3e460cddb83eacc1a012aebd009cd087ba1b68d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594142"
---
# <span data-ttu-id="89761-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89761-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="89761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89761-102">SYNOPSIS</span></span>
<span data-ttu-id="89761-103">Toplu hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89761-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89761-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89761-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89761-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89761-105">DESCRIPTION</span></span>
<span data-ttu-id="89761-106">**Remove-AzureRmBatchAccount** cmdlet 'ı bir Azure toplu hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89761-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="89761-107">*Force* parametresini belirtmediğiniz sürece, bu cmdlet bir hesabı kaldırmadan önce size sorar.</span><span class="sxs-lookup"><span data-stu-id="89761-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="89761-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89761-108">EXAMPLES</span></span>

### <span data-ttu-id="89761-109">Örnek 1: toplu Iş hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="89761-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="89761-110">Bu komut, pfuller adlı toplu hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89761-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="89761-111">Bu komut, hesabı silmeden önce onayınızı ister.</span><span class="sxs-lookup"><span data-stu-id="89761-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="89761-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89761-112">PARAMETERS</span></span>

### <span data-ttu-id="89761-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89761-113">-AccountName</span></span>
<span data-ttu-id="89761-114">Bu cmdlet 'in kaldırdığı toplu hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89761-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89761-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89761-115">-DefaultProfile</span></span>
<span data-ttu-id="89761-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89761-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89761-117">-Force</span><span class="sxs-lookup"><span data-stu-id="89761-117">-Force</span></span>
<span data-ttu-id="89761-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="89761-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89761-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89761-119">-ResourceGroupName</span></span>
<span data-ttu-id="89761-120">Bu cmdlet 'in kaldırdığı hesabın kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="89761-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89761-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="89761-121">-Confirm</span></span>
<span data-ttu-id="89761-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89761-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89761-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89761-123">-WhatIf</span></span>
<span data-ttu-id="89761-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89761-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89761-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89761-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89761-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89761-126">CommonParameters</span></span>
<span data-ttu-id="89761-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89761-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89761-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89761-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89761-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89761-129">INPUTS</span></span>

### <span data-ttu-id="89761-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="89761-130">None</span></span>
<span data-ttu-id="89761-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="89761-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89761-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89761-132">OUTPUTS</span></span>

## <span data-ttu-id="89761-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89761-133">NOTES</span></span>

## <span data-ttu-id="89761-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89761-134">RELATED LINKS</span></span>

[<span data-ttu-id="89761-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89761-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="89761-136">Yeni-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89761-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="89761-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="89761-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="89761-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="89761-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


