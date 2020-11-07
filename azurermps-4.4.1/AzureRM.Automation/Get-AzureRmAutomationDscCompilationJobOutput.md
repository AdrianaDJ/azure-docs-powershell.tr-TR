---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: d38971c15c46cbeaba6e9dda87ad0f3b7febbfd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592677"
---
# <span data-ttu-id="e1500-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e1500-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="e1500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1500-102">SYNOPSIS</span></span>
<span data-ttu-id="e1500-103">Bir Automation DSC derleme işinin günlüğe kaydetme akışlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e1500-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1500-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1500-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1500-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1500-105">DESCRIPTION</span></span>
<span data-ttu-id="e1500-106">**Get-Azurermautomationdsccompilationjoi Input** cmdlet 'i, bir APS için</span><span class="sxs-lookup"><span data-stu-id="e1500-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="e1500-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1500-107">EXAMPLES</span></span>

### <span data-ttu-id="e1500-108">Örnek 1: DSC derleme işi için günlükleri alma</span><span class="sxs-lookup"><span data-stu-id="e1500-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="e1500-109">İlk komut, Get-AzureRmAutomationDscCompilationJob cmdlet 'ini kullanarak Contoso17 adlı Otomasyon hesabındaki derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e1500-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="e1500-110">Komut bu nesneleri $Jobs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e1500-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="e1500-111">İkinci komut $Jobs dizisinin ilk üyesinin tüm akışı için derleme işi çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="e1500-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="e1500-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1500-112">PARAMETERS</span></span>

### <span data-ttu-id="e1500-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1500-113">-AutomationAccountName</span></span>
<span data-ttu-id="e1500-114">DSC derleme işini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1500-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1500-115">-ID</span><span class="sxs-lookup"><span data-stu-id="e1500-115">-Id</span></span>
<span data-ttu-id="e1500-116">Bu cmdlet 'in çıkışı aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1500-116">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1500-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1500-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1500-118">Bu cmdlet 'in akış kayıtlarını aldığı DSC derleme işini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1500-118">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1500-119">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e1500-119">-StartTime</span></span>
<span data-ttu-id="e1500-120">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1500-120">Specifies a start time.</span></span>
<span data-ttu-id="e1500-121">Bu cmdlet, DSC derleme işinin bu süreden sonra aldığı akış kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e1500-121">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1500-122">-Stream</span><span class="sxs-lookup"><span data-stu-id="e1500-122">-Stream</span></span>
<span data-ttu-id="e1500-123">Bu cmdlet 'in aldığı çıktı için akış türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1500-123">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="e1500-124">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e1500-124">Valid values are:</span></span> 

- <span data-ttu-id="e1500-125">Tüm</span><span class="sxs-lookup"><span data-stu-id="e1500-125">Any</span></span> 
- <span data-ttu-id="e1500-126">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="e1500-126">Warning</span></span> 
- <span data-ttu-id="e1500-127">Hatalar</span><span class="sxs-lookup"><span data-stu-id="e1500-127">Error</span></span> 
- <span data-ttu-id="e1500-128">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="e1500-128">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1500-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1500-129">-DefaultProfile</span></span>
<span data-ttu-id="e1500-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1500-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1500-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1500-131">CommonParameters</span></span>
<span data-ttu-id="e1500-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1500-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1500-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1500-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1500-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1500-134">INPUTS</span></span>

## <span data-ttu-id="e1500-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1500-135">OUTPUTS</span></span>

### <span data-ttu-id="e1500-136">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="e1500-136">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="e1500-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1500-137">NOTES</span></span>

## <span data-ttu-id="e1500-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1500-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1500-139">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e1500-139">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="e1500-140">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e1500-140">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

