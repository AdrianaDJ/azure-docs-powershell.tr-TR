---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: e7093f04cfd7b51f00dcc5cbcd6ad3cb98f54bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595118"
---
# <span data-ttu-id="14429-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="14429-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="14429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14429-102">SYNOPSIS</span></span>
<span data-ttu-id="14429-103">Bir Automation DSC derleme işinin günlüğe kaydetme akışlarını alır.</span><span class="sxs-lookup"><span data-stu-id="14429-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14429-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14429-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14429-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14429-105">DESCRIPTION</span></span>
<span data-ttu-id="14429-106">**Get-Azurermautomationdsccompilationjoi Input** cmdlet 'i, bir APS için</span><span class="sxs-lookup"><span data-stu-id="14429-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="14429-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14429-107">EXAMPLES</span></span>

### <span data-ttu-id="14429-108">Örnek 1: DSC derleme işi için günlükleri alma</span><span class="sxs-lookup"><span data-stu-id="14429-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="14429-109">İlk komut, Get-AzureRmAutomationDscCompilationJob cmdlet 'ini kullanarak Contoso17 adlı Otomasyon hesabındaki derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="14429-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="14429-110">Komut bu nesneleri $Jobs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="14429-110">The command stores those objects in the $Jobs variable.</span></span>

<span data-ttu-id="14429-111">İkinci komut $Jobs dizisinin ilk üyesinin tüm akışı için derleme işi çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="14429-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="14429-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14429-112">PARAMETERS</span></span>

### <span data-ttu-id="14429-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="14429-113">-AutomationAccountName</span></span>
<span data-ttu-id="14429-114">DSC derleme işini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14429-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14429-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14429-115">-DefaultProfile</span></span>
<span data-ttu-id="14429-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="14429-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14429-117">-ID</span><span class="sxs-lookup"><span data-stu-id="14429-117">-Id</span></span>
<span data-ttu-id="14429-118">Bu cmdlet 'in çıkışı aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="14429-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14429-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14429-119">-ResourceGroupName</span></span>
<span data-ttu-id="14429-120">Bu cmdlet 'in akış kayıtlarını aldığı DSC derleme işini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14429-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14429-121">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="14429-121">-StartTime</span></span>
<span data-ttu-id="14429-122">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14429-122">Specifies a start time.</span></span>
<span data-ttu-id="14429-123">Bu cmdlet, DSC derleme işinin bu süreden sonra aldığı akış kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="14429-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="14429-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="14429-124">-Stream</span></span>
<span data-ttu-id="14429-125">Bu cmdlet 'in aldığı çıktı için akış türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="14429-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="14429-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="14429-126">Valid values are:</span></span> 

- <span data-ttu-id="14429-127">Tüm</span><span class="sxs-lookup"><span data-stu-id="14429-127">Any</span></span> 
- <span data-ttu-id="14429-128">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="14429-128">Warning</span></span> 
- <span data-ttu-id="14429-129">Hatalar</span><span class="sxs-lookup"><span data-stu-id="14429-129">Error</span></span> 
- <span data-ttu-id="14429-130">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="14429-130">Verbose</span></span>

```yaml
Type: CompilationJobStreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14429-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14429-131">CommonParameters</span></span>
<span data-ttu-id="14429-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14429-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14429-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14429-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14429-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14429-134">INPUTS</span></span>

### <span data-ttu-id="14429-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14429-135">None</span></span>
<span data-ttu-id="14429-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="14429-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14429-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14429-137">OUTPUTS</span></span>

### <span data-ttu-id="14429-138">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="14429-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="14429-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14429-139">NOTES</span></span>

## <span data-ttu-id="14429-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14429-140">RELATED LINKS</span></span>

[<span data-ttu-id="14429-141">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="14429-141">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="14429-142">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="14429-142">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


