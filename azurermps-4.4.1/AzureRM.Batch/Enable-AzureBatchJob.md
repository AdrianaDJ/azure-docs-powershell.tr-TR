---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764905"
---
# <span data-ttu-id="50c9b-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="50c9b-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="50c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="50c9b-103">Toplu işi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="50c9b-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50c9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50c9b-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50c9b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="50c9b-106">**Enable-AzureBatchJob** cmdlet 'ı bir Azure toplu işine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="50c9b-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="50c9b-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="50c9b-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="50c9b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50c9b-108">EXAMPLES</span></span>

### <span data-ttu-id="50c9b-109">Örnek 1: bir toplu işi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="50c9b-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="50c9b-110">Bu komut, Iş-000001 KIMLIĞINE sahip işi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="50c9b-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="50c9b-111">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="50c9b-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="50c9b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50c9b-112">PARAMETERS</span></span>

### <span data-ttu-id="50c9b-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="50c9b-113">-BatchContext</span></span>
<span data-ttu-id="50c9b-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50c9b-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="50c9b-115">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="50c9b-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50c9b-116">-ID</span><span class="sxs-lookup"><span data-stu-id="50c9b-116">-Id</span></span>
<span data-ttu-id="50c9b-117">Bu cmdlet 'in etkinleştirmesine iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="50c9b-117">Specifies the ID of the job that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50c9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c9b-118">-DefaultProfile</span></span>
<span data-ttu-id="50c9b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50c9b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c9b-120">CommonParameters</span></span>
<span data-ttu-id="50c9b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50c9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c9b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c9b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c9b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50c9b-123">INPUTS</span></span>

### <span data-ttu-id="50c9b-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="50c9b-124">BatchAccountContext</span></span>
<span data-ttu-id="50c9b-125">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="50c9b-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="50c9b-126">Dizisi</span><span class="sxs-lookup"><span data-stu-id="50c9b-126">String</span></span>
<span data-ttu-id="50c9b-127">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="50c9b-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="50c9b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50c9b-128">OUTPUTS</span></span>

## <span data-ttu-id="50c9b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50c9b-129">NOTES</span></span>

## <span data-ttu-id="50c9b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50c9b-130">RELATED LINKS</span></span>

[<span data-ttu-id="50c9b-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="50c9b-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="50c9b-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="50c9b-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="50c9b-133">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="50c9b-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="50c9b-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="50c9b-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="50c9b-135">Stop-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="50c9b-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="50c9b-136">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="50c9b-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


