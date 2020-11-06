---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: C06D4AD3-9CB1-4FEB-B02F-74022F264260
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/disable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Disable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: c754b7e30fdec3a179beefdf48292a781ec083db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589680"
---
# <span data-ttu-id="59745-101">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59745-101">Disable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="59745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59745-102">SYNOPSIS</span></span>
<span data-ttu-id="59745-103">İş koleksiyonunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="59745-103">Disables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59745-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59745-104">SYNTAX</span></span>

```
Disable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59745-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59745-105">DESCRIPTION</span></span>
<span data-ttu-id="59745-106">**Disable-AzureRmSchedulerJobCollection** cmdlet 'ı, Azure Zamanlayıcısı 'nda bir iş koleksiyonunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="59745-106">The **Disable-AzureRmSchedulerJobCollection** cmdlet disables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="59745-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59745-107">EXAMPLES</span></span>

## <span data-ttu-id="59745-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59745-108">PARAMETERS</span></span>

### <span data-ttu-id="59745-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59745-109">-DefaultProfile</span></span>
<span data-ttu-id="59745-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59745-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59745-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="59745-111">-JobCollectionName</span></span>
<span data-ttu-id="59745-112">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59745-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="59745-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59745-113">-PassThru</span></span>
<span data-ttu-id="59745-114">Bu cmdlet 'in başarı durumunda başarı değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="59745-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="59745-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="59745-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59745-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59745-116">-ResourceGroupName</span></span>
<span data-ttu-id="59745-117">İş koleksiyonunun kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59745-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="59745-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="59745-118">-Confirm</span></span>
<span data-ttu-id="59745-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59745-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59745-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59745-120">-WhatIf</span></span>
<span data-ttu-id="59745-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59745-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59745-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59745-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59745-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59745-123">CommonParameters</span></span>
<span data-ttu-id="59745-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59745-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59745-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59745-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59745-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59745-126">INPUTS</span></span>

### <span data-ttu-id="59745-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59745-127">None</span></span>
<span data-ttu-id="59745-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="59745-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59745-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59745-129">OUTPUTS</span></span>

## <span data-ttu-id="59745-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59745-130">NOTES</span></span>

## <span data-ttu-id="59745-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59745-131">RELATED LINKS</span></span>

[<span data-ttu-id="59745-132">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59745-132">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="59745-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59745-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="59745-134">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59745-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="59745-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59745-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="59745-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="59745-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


