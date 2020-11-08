---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106553"
---
# <span data-ttu-id="23d53-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="23d53-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="23d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d53-102">SYNOPSIS</span></span>
<span data-ttu-id="23d53-103">Yürütme veya geri alma işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d53-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="23d53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23d53-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23d53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23d53-105">DESCRIPTION</span></span>
<span data-ttu-id="23d53-106">**Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet 'i, Commit veya Rollback işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d53-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="23d53-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23d53-107">EXAMPLES</span></span>

### <span data-ttu-id="23d53-108">Örnek 1: tamamlanan bir yürütme işleminin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="23d53-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="23d53-109">Bu komut, adlandırılmış kapsayıcı için bir yürütme işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d53-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="23d53-110">Bu işlemin durumu tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="23d53-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="23d53-111">Örnek 2: tamamlanmış bir geri alma işleminin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="23d53-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="23d53-112">Bu komut, adlandırılmış kapsayıcı için geri alma işleminin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="23d53-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="23d53-113">Bu işlemin durumu tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="23d53-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="23d53-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23d53-114">PARAMETERS</span></span>

### <span data-ttu-id="23d53-115">-Legacyconfigıd</span><span class="sxs-lookup"><span data-stu-id="23d53-115">-LegacyConfigId</span></span>
<span data-ttu-id="23d53-116">Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d53-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d53-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="23d53-117">-LegacyContainerNames</span></span>
<span data-ttu-id="23d53-118">Geçiş planının uygulandığı birim kapsayıcı adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d53-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d53-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="23d53-119">-Profile</span></span>
<span data-ttu-id="23d53-120">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="23d53-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="23d53-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d53-121">CommonParameters</span></span>
<span data-ttu-id="23d53-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23d53-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d53-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d53-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d53-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23d53-124">INPUTS</span></span>

### <span data-ttu-id="23d53-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23d53-125">None</span></span>

## <span data-ttu-id="23d53-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23d53-126">OUTPUTS</span></span>

### <span data-ttu-id="23d53-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="23d53-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="23d53-128">Bu cmdlet, gerçekleştirilen geçiş Onayla işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="23d53-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="23d53-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23d53-129">NOTES</span></span>

## <span data-ttu-id="23d53-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23d53-130">RELATED LINKS</span></span>

[<span data-ttu-id="23d53-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="23d53-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="23d53-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="23d53-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


