---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: a5de80561ee0b80c2ce825db26e1de5c6f46b80b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588593"
---
# <span data-ttu-id="6b02b-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b02b-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="6b02b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b02b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b02b-103">Yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="6b02b-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b02b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b02b-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b02b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b02b-105">DESCRIPTION</span></span>
<span data-ttu-id="6b02b-106">**Wait-AzureRmBackupJob** cmdlet 'ı bir Azure yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="6b02b-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="6b02b-107">Yedekleme işleri uzun zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="6b02b-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="6b02b-108">Bir yedekleme işini bir komut dosyasının parçası olarak çalıştırırsanız, diğer görevlere devam etmeden önce bu komut dosyasının işin bitmesini beklemeye zorlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b02b-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="6b02b-109">Bu cmdlet 'i içeren bir komut dosyası, iş durumu için yedekleme hizmetini yoklayıp birden kolay olabilir.</span><span class="sxs-lookup"><span data-stu-id="6b02b-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="6b02b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b02b-110">EXAMPLES</span></span>

## <span data-ttu-id="6b02b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b02b-111">PARAMETERS</span></span>

### <span data-ttu-id="6b02b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b02b-112">-DefaultProfile</span></span>
<span data-ttu-id="6b02b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6b02b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b02b-114">-Job</span><span class="sxs-lookup"><span data-stu-id="6b02b-114">-Job</span></span>
<span data-ttu-id="6b02b-115">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b02b-115">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="6b02b-116">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6b02b-116">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="6b02b-117">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="6b02b-117">-TimeOut</span></span>
<span data-ttu-id="6b02b-118">Bu cmdlet işin bitmesini beklediği en uzun süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b02b-118">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="6b02b-119">Zaman aşımı değeri belirtmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="6b02b-119">We recommend that you specify a time-out value.</span></span>

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

### <span data-ttu-id="6b02b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b02b-120">CommonParameters</span></span>
<span data-ttu-id="6b02b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b02b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b02b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b02b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b02b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b02b-123">INPUTS</span></span>

### <span data-ttu-id="6b02b-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="6b02b-124">System.Object</span></span>
<span data-ttu-id="6b02b-125">Parametreler: Iş (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b02b-125">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="6b02b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b02b-126">OUTPUTS</span></span>

### <span data-ttu-id="6b02b-127">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b02b-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="6b02b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b02b-128">NOTES</span></span>

## <span data-ttu-id="6b02b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b02b-129">RELATED LINKS</span></span>

[<span data-ttu-id="6b02b-130">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b02b-130">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="6b02b-131">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b02b-131">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


