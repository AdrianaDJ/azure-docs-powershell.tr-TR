---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593595"
---
# <span data-ttu-id="78388-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="78388-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="78388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78388-102">SYNOPSIS</span></span>
<span data-ttu-id="78388-103">Yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="78388-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78388-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78388-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78388-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="78388-105">DESCRIPTION</span></span>
<span data-ttu-id="78388-106">**Wait-AzureRmBackupJob** cmdlet 'ı bir Azure yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="78388-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="78388-107">Yedekleme işleri uzun zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="78388-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="78388-108">Bir yedekleme işini bir komut dosyasının parçası olarak çalıştırırsanız, diğer görevlere devam etmeden önce bu komut dosyasının işin bitmesini beklemeye zorlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78388-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="78388-109">Bu cmdlet 'i içeren bir komut dosyası, iş durumu için yedekleme hizmetini yoklayıp birden kolay olabilir.</span><span class="sxs-lookup"><span data-stu-id="78388-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="78388-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78388-110">EXAMPLES</span></span>

## <span data-ttu-id="78388-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78388-111">PARAMETERS</span></span>

### <span data-ttu-id="78388-112">-Job</span><span class="sxs-lookup"><span data-stu-id="78388-112">-Job</span></span>
<span data-ttu-id="78388-113">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="78388-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="78388-114">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="78388-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78388-115">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="78388-115">-TimeOut</span></span>
<span data-ttu-id="78388-116">Bu cmdlet işin bitmesini beklediği en uzun süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="78388-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="78388-117">Zaman aşımı değeri belirtmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="78388-117">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78388-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78388-118">-DefaultProfile</span></span>
<span data-ttu-id="78388-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78388-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78388-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78388-120">CommonParameters</span></span>
<span data-ttu-id="78388-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78388-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78388-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78388-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78388-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78388-123">INPUTS</span></span>

### <span data-ttu-id="78388-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="78388-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="78388-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78388-125">OUTPUTS</span></span>

### <span data-ttu-id="78388-126">AzureRmBackupJob []</span><span class="sxs-lookup"><span data-stu-id="78388-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="78388-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78388-127">NOTES</span></span>

## <span data-ttu-id="78388-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78388-128">RELATED LINKS</span></span>

[<span data-ttu-id="78388-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="78388-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="78388-130">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="78388-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


