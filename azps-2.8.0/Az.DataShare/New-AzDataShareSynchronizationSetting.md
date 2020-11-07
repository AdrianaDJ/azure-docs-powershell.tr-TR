---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: ba8f51832aada036363dea95a8f604b24966e76b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752180"
---
# <span data-ttu-id="472b7-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="472b7-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="472b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="472b7-102">SYNOPSIS</span></span>
<span data-ttu-id="472b7-103">Paylaşım için eşitleme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="472b7-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="472b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="472b7-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="472b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="472b7-105">DESCRIPTION</span></span>
<span data-ttu-id="472b7-106">**Yeni-Azverisharesyntarihçe ayarı** , belirli bir zamanda günlük veya saatlik olarak saat yinelemesi için paylaşım hesabında paylaşım için bir eşitleme ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="472b7-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="472b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="472b7-107">EXAMPLES</span></span>

### <span data-ttu-id="472b7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="472b7-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="472b7-109">Bu 9:00 komut, veri paylaşımı hesap kutucuğundaki Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="472b7-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="472b7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="472b7-110">PARAMETERS</span></span>

### <span data-ttu-id="472b7-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="472b7-111">-AccountName</span></span>
<span data-ttu-id="472b7-112">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="472b7-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472b7-113">-DefaultProfile</span></span>
<span data-ttu-id="472b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="472b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="472b7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="472b7-115">-Name</span></span>
<span data-ttu-id="472b7-116">Eşitleme ayarı adı</span><span class="sxs-lookup"><span data-stu-id="472b7-116">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472b7-117">-Recurrenceınterval</span><span class="sxs-lookup"><span data-stu-id="472b7-117">-RecurrenceInterval</span></span>
<span data-ttu-id="472b7-118">Eşitleme ayarının tekrarlama aralığı (gün veya saat)</span><span class="sxs-lookup"><span data-stu-id="472b7-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="472b7-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="472b7-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472b7-121">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="472b7-121">-ShareName</span></span>
<span data-ttu-id="472b7-122">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="472b7-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472b7-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="472b7-123">-SynchronizationTime</span></span>
<span data-ttu-id="472b7-124">Zamanlanan eşitleme ayarının başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="472b7-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="472b7-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="472b7-125">-Confirm</span></span>
<span data-ttu-id="472b7-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="472b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="472b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472b7-127">-WhatIf</span></span>
<span data-ttu-id="472b7-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="472b7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="472b7-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="472b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="472b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472b7-130">CommonParameters</span></span>
<span data-ttu-id="472b7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="472b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472b7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="472b7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472b7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="472b7-133">INPUTS</span></span>

### <span data-ttu-id="472b7-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="472b7-134">None</span></span>

## <span data-ttu-id="472b7-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="472b7-135">OUTPUTS</span></span>

### <span data-ttu-id="472b7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSData</span><span class="sxs-lookup"><span data-stu-id="472b7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="472b7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="472b7-137">NOTES</span></span>

## <span data-ttu-id="472b7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="472b7-138">RELATED LINKS</span></span>