---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b4ff486bac10c79a544761c1946fd3e34dce69a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763546"
---
# <span data-ttu-id="8de82-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8de82-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="8de82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de82-102">SYNOPSIS</span></span>
<span data-ttu-id="8de82-103">İş koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8de82-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8de82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8de82-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de82-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8de82-105">DESCRIPTION</span></span>
<span data-ttu-id="8de82-106">**Remove-AzureRmSchedulerJobCollection** cmdlet 'ı, Azure Zamanlayıcısı 'ndaki bir iş koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8de82-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="8de82-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8de82-107">EXAMPLES</span></span>

## <span data-ttu-id="8de82-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8de82-108">PARAMETERS</span></span>

### <span data-ttu-id="8de82-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de82-109">-DefaultProfile</span></span>
<span data-ttu-id="8de82-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8de82-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8de82-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8de82-111">-JobCollectionName</span></span>
<span data-ttu-id="8de82-112">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8de82-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de82-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8de82-113">-PassThru</span></span>
<span data-ttu-id="8de82-114">Bu cmdlet 'in başarı durumunda başarı değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="8de82-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="8de82-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8de82-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8de82-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de82-116">-ResourceGroupName</span></span>
<span data-ttu-id="8de82-117">İş koleksiyonunun kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8de82-117">Specifies the resource group of the job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de82-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="8de82-118">-Confirm</span></span>
<span data-ttu-id="8de82-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8de82-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de82-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de82-120">-WhatIf</span></span>
<span data-ttu-id="8de82-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8de82-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de82-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8de82-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de82-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de82-123">CommonParameters</span></span>
<span data-ttu-id="8de82-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8de82-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de82-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de82-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de82-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8de82-126">INPUTS</span></span>

### <span data-ttu-id="8de82-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8de82-127">None</span></span>
<span data-ttu-id="8de82-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8de82-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8de82-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8de82-129">OUTPUTS</span></span>

## <span data-ttu-id="8de82-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8de82-130">NOTES</span></span>

## <span data-ttu-id="8de82-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8de82-131">RELATED LINKS</span></span>

[<span data-ttu-id="8de82-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8de82-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8de82-133">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8de82-133">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8de82-134">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8de82-134">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8de82-135">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8de82-135">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8de82-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8de82-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


