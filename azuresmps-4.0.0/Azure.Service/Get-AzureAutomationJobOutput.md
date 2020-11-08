---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105658"
---
# <span data-ttu-id="461c7-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="461c7-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="461c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="461c7-102">SYNOPSIS</span></span>

<span data-ttu-id="461c7-103">Bir Azure Otomasyonu işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="461c7-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="461c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="461c7-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="461c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="461c7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="461c7-106">**Get-Azureautomationjoi Input** cmdlet 'ı bir Microsoft Azure Otomasyonu işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="461c7-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="461c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="461c7-107">EXAMPLES</span></span>

### <span data-ttu-id="461c7-108">Örnek 1: Azure Otomasyonu işinin çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="461c7-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="461c7-109">Bu komut, işin belirtilen KIMLIĞINE sahip olan tüm çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="461c7-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="461c7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="461c7-110">PARAMETERS</span></span>

### <span data-ttu-id="461c7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="461c7-111">-AutomationAccountName</span></span>
<span data-ttu-id="461c7-112">Azure Otomasyonu hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="461c7-112">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="461c7-113">-ID</span><span class="sxs-lookup"><span data-stu-id="461c7-113">-Id</span></span>
<span data-ttu-id="461c7-114">İşin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="461c7-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="461c7-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="461c7-115">-Profile</span></span>
<span data-ttu-id="461c7-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="461c7-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="461c7-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="461c7-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461c7-118">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="461c7-118">-StartTime</span></span>
<span data-ttu-id="461c7-119">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="461c7-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="461c7-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="461c7-120">-Stream</span></span>
<span data-ttu-id="461c7-121">Çıktının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="461c7-121">Specifies the type of output.</span></span>
<span data-ttu-id="461c7-122">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="461c7-122">Valid values are:</span></span> 

- <span data-ttu-id="461c7-123">Tüm</span><span class="sxs-lookup"><span data-stu-id="461c7-123">Any</span></span>
- <span data-ttu-id="461c7-124">Hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="461c7-124">Debug</span></span>
- <span data-ttu-id="461c7-125">Hatalar</span><span class="sxs-lookup"><span data-stu-id="461c7-125">Error</span></span>
- <span data-ttu-id="461c7-126">Çıkışının</span><span class="sxs-lookup"><span data-stu-id="461c7-126">Output</span></span>
- <span data-ttu-id="461c7-127">Sürdüğü</span><span class="sxs-lookup"><span data-stu-id="461c7-127">Progress</span></span>
- <span data-ttu-id="461c7-128">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="461c7-128">Verbose</span></span>
- <span data-ttu-id="461c7-129">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="461c7-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="461c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461c7-130">CommonParameters</span></span>
<span data-ttu-id="461c7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="461c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461c7-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="461c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461c7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="461c7-133">INPUTS</span></span>

## <span data-ttu-id="461c7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="461c7-134">OUTPUTS</span></span>

## <span data-ttu-id="461c7-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="461c7-135">NOTES</span></span>

## <span data-ttu-id="461c7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="461c7-136">RELATED LINKS</span></span>

[<span data-ttu-id="461c7-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="461c7-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="461c7-138">Özgeçmiş-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="461c7-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="461c7-139">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="461c7-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="461c7-140">Askıya alma-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="461c7-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


