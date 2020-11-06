---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: de8f9e05cbec17d6a92f3c4e567bd5dce96005ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591615"
---
# <span data-ttu-id="cb727-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="cb727-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="cb727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb727-102">SYNOPSIS</span></span>
<span data-ttu-id="cb727-103">Zamanlayıcı işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb727-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb727-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb727-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb727-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb727-105">DESCRIPTION</span></span>
<span data-ttu-id="cb727-106">**Remove-AzureRmSchedulerJob** cmdlet 'ı bir Azure Zamanlayıcı işini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb727-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="cb727-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb727-107">EXAMPLES</span></span>

## <span data-ttu-id="cb727-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb727-108">PARAMETERS</span></span>

### <span data-ttu-id="cb727-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb727-109">-DefaultProfile</span></span>
<span data-ttu-id="cb727-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb727-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb727-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="cb727-111">-JobCollectionName</span></span>
<span data-ttu-id="cb727-112">Kaldırılacak işi içeren bir iş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb727-112">Specifies the name of a job collection that contains the job to remove.</span></span>

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

### <span data-ttu-id="cb727-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="cb727-113">-JobName</span></span>
<span data-ttu-id="cb727-114">Kaldırılacak işin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb727-114">Specifies the name of a job to remove.</span></span>

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

### <span data-ttu-id="cb727-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb727-115">-PassThru</span></span>
<span data-ttu-id="cb727-116">Bu cmdlet 'in başarı durumunda başarı değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="cb727-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="cb727-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cb727-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb727-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb727-118">-ResourceGroupName</span></span>
<span data-ttu-id="cb727-119">Kaldırılacak işin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb727-119">Specifies the resource group of the job to remove.</span></span>

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

### <span data-ttu-id="cb727-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb727-120">-Confirm</span></span>
<span data-ttu-id="cb727-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb727-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb727-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb727-122">-WhatIf</span></span>
<span data-ttu-id="cb727-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb727-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb727-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb727-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb727-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb727-125">CommonParameters</span></span>
<span data-ttu-id="cb727-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb727-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb727-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb727-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb727-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb727-128">INPUTS</span></span>

### <span data-ttu-id="cb727-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cb727-129">None</span></span>
<span data-ttu-id="cb727-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cb727-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb727-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb727-131">OUTPUTS</span></span>

## <span data-ttu-id="cb727-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb727-132">NOTES</span></span>

## <span data-ttu-id="cb727-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb727-133">RELATED LINKS</span></span>

[<span data-ttu-id="cb727-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="cb727-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


