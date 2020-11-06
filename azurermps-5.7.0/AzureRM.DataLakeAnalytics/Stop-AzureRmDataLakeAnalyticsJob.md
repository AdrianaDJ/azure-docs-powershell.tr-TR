---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589812"
---
# <span data-ttu-id="a057e-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a057e-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a057e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a057e-102">SYNOPSIS</span></span>
<span data-ttu-id="a057e-103">İşi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a057e-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a057e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a057e-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a057e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a057e-105">DESCRIPTION</span></span>
<span data-ttu-id="a057e-106">**Stop-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a057e-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="a057e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a057e-107">EXAMPLES</span></span>

### <span data-ttu-id="a057e-108">Örnek 1: işi Iptal etme</span><span class="sxs-lookup"><span data-stu-id="a057e-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="a057e-109">Bu komut belirtilen KIMLIĞE sahip işi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a057e-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="a057e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a057e-110">PARAMETERS</span></span>

### <span data-ttu-id="a057e-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="a057e-111">-Account</span></span>
<span data-ttu-id="a057e-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a057e-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a057e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a057e-113">-DefaultProfile</span></span>
<span data-ttu-id="a057e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a057e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a057e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a057e-115">-Force</span></span>
<span data-ttu-id="a057e-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a057e-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a057e-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="a057e-117">-JobId</span></span>
<span data-ttu-id="a057e-118">İptal edilecek işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a057e-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a057e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a057e-119">-PassThru</span></span>
<span data-ttu-id="a057e-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a057e-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a057e-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a057e-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a057e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a057e-122">-Confirm</span></span>
<span data-ttu-id="a057e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a057e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a057e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a057e-124">-WhatIf</span></span>
<span data-ttu-id="a057e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a057e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a057e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a057e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a057e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a057e-127">CommonParameters</span></span>
<span data-ttu-id="a057e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a057e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a057e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a057e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a057e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a057e-130">INPUTS</span></span>

### <span data-ttu-id="a057e-131">'Sine</span><span class="sxs-lookup"><span data-stu-id="a057e-131">Guid</span></span>
<span data-ttu-id="a057e-132">' JobId ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a057e-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="a057e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a057e-133">OUTPUTS</span></span>

### <span data-ttu-id="a057e-134">bool</span><span class="sxs-lookup"><span data-stu-id="a057e-134">bool</span></span>
<span data-ttu-id="a057e-135">Geçiş belirtildiyse, işlem tamamlandığında doğru değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a057e-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="a057e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a057e-136">NOTES</span></span>

## <span data-ttu-id="a057e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a057e-137">RELATED LINKS</span></span>

[<span data-ttu-id="a057e-138">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="a057e-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a057e-139">Submit-Azurermdatalakeanalyzer Ticsjob</span><span class="sxs-lookup"><span data-stu-id="a057e-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a057e-140">Wait-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="a057e-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


