---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096071"
---
# <span data-ttu-id="ab191-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab191-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="ab191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab191-102">SYNOPSIS</span></span>
<span data-ttu-id="ab191-103">İşi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="ab191-103">Cancels a job.</span></span>

## <span data-ttu-id="ab191-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab191-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab191-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab191-105">DESCRIPTION</span></span>
<span data-ttu-id="ab191-106">**Stop-Azdatalakeanaliz Ticsjob** cmdlet 'ı bir Azure Data Lake Analytics işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="ab191-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="ab191-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab191-107">EXAMPLES</span></span>

### <span data-ttu-id="ab191-108">Örnek 1: işi Iptal etme</span><span class="sxs-lookup"><span data-stu-id="ab191-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="ab191-109">Bu komut belirtilen KIMLIĞE sahip işi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="ab191-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="ab191-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab191-110">PARAMETERS</span></span>

### <span data-ttu-id="ab191-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="ab191-111">-Account</span></span>
<span data-ttu-id="ab191-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab191-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab191-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab191-113">-DefaultProfile</span></span>
<span data-ttu-id="ab191-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ab191-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab191-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ab191-115">-Force</span></span>
<span data-ttu-id="ab191-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ab191-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab191-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="ab191-117">-JobId</span></span>
<span data-ttu-id="ab191-118">İptal edilecek işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab191-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab191-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ab191-119">-PassThru</span></span>
<span data-ttu-id="ab191-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ab191-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ab191-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ab191-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab191-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab191-122">-Confirm</span></span>
<span data-ttu-id="ab191-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab191-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab191-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab191-124">-WhatIf</span></span>
<span data-ttu-id="ab191-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab191-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab191-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab191-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab191-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab191-127">CommonParameters</span></span>
<span data-ttu-id="ab191-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab191-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab191-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab191-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab191-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab191-130">INPUTS</span></span>

### <span data-ttu-id="ab191-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ab191-131">System.String</span></span>

### <span data-ttu-id="ab191-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="ab191-132">System.Guid</span></span>

### <span data-ttu-id="ab191-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab191-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab191-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab191-134">OUTPUTS</span></span>

### <span data-ttu-id="ab191-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab191-135">System.Boolean</span></span>

## <span data-ttu-id="ab191-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab191-136">NOTES</span></span>

## <span data-ttu-id="ab191-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab191-137">RELATED LINKS</span></span>

[<span data-ttu-id="ab191-138">Get-Azdatalakeçözümlerken</span><span class="sxs-lookup"><span data-stu-id="ab191-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ab191-139">Submit-Azdatalakeanaliz Ticsjob</span><span class="sxs-lookup"><span data-stu-id="ab191-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="ab191-140">Wait-Azdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="ab191-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)

