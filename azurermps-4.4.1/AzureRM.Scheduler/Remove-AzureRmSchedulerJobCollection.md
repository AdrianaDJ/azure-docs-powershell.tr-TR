---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F315B193-C17B-41A9-B61D-0A0212B6B643
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: b1caa041f92312d3d122e758a9e63bc7299887b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590651"
---
# <span data-ttu-id="0bd2a-101">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0bd2a-101">Remove-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="0bd2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bd2a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd2a-103">İş koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-103">Removes a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bd2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0bd2a-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0bd2a-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd2a-106">**Remove-AzureRmSchedulerJobCollection** cmdlet 'ı, Azure Zamanlayıcısı 'ndaki bir iş koleksiyonunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-106">The **Remove-AzureRmSchedulerJobCollection** cmdlet removes a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="0bd2a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0bd2a-107">EXAMPLES</span></span>

## <span data-ttu-id="0bd2a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0bd2a-108">PARAMETERS</span></span>

### <span data-ttu-id="0bd2a-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0bd2a-109">-JobCollectionName</span></span>
<span data-ttu-id="0bd2a-110">İş koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd2a-111">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0bd2a-111">-PassThru</span></span>
<span data-ttu-id="0bd2a-112">Bu cmdlet 'in başarı durumunda başarı değeri döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-112">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="0bd2a-113">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bd2a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd2a-114">-ResourceGroupName</span></span>
<span data-ttu-id="0bd2a-115">İş koleksiyonunun kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-115">Specifies the resource group of the job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bd2a-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="0bd2a-116">-Confirm</span></span>
<span data-ttu-id="0bd2a-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bd2a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bd2a-118">-WhatIf</span></span>
<span data-ttu-id="0bd2a-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bd2a-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bd2a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd2a-121">-DefaultProfile</span></span>
<span data-ttu-id="0bd2a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bd2a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd2a-123">CommonParameters</span></span>
<span data-ttu-id="0bd2a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0bd2a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd2a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd2a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd2a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0bd2a-126">INPUTS</span></span>

## <span data-ttu-id="0bd2a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0bd2a-127">OUTPUTS</span></span>

## <span data-ttu-id="0bd2a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0bd2a-128">NOTES</span></span>

## <span data-ttu-id="0bd2a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0bd2a-129">RELATED LINKS</span></span>

[<span data-ttu-id="0bd2a-130">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0bd2a-130">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0bd2a-131">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0bd2a-131">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0bd2a-132">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0bd2a-132">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0bd2a-133">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0bd2a-133">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0bd2a-134">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0bd2a-134">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


