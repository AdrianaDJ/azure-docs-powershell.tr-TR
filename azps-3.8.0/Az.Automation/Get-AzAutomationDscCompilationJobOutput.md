---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJobOutput.md
ms.openlocfilehash: 259f79e68b67726f78c96c46d62f8efbb2390d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098183"
---
# <span data-ttu-id="51476-101">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="51476-101">Get-AzAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="51476-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51476-102">SYNOPSIS</span></span>
<span data-ttu-id="51476-103">Bir Automation DSC derleme işinin günlüğe kaydetme akışlarını alır.</span><span class="sxs-lookup"><span data-stu-id="51476-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

## <span data-ttu-id="51476-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51476-104">SYNTAX</span></span>

```
Get-AzAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51476-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51476-105">DESCRIPTION</span></span>
<span data-ttu-id="51476-106">**Get-Azautomationdsccompilationjoi Input** cmdlet 'i, bir APS Istenen durum yapılandırma (DSC) derleme işinin akış kayıtlarını, Azure Otomasyonu 'nda alır.</span><span class="sxs-lookup"><span data-stu-id="51476-106">The **Get-AzAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="51476-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51476-107">EXAMPLES</span></span>

### <span data-ttu-id="51476-108">Örnek 1: DSC derleme işi için günlükleri alma</span><span class="sxs-lookup"><span data-stu-id="51476-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="51476-109">İlk komut, Get-AzAutomationDscCompilationJob cmdlet 'ini kullanarak Contoso17 adlı Otomasyon hesabındaki derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="51476-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="51476-110">Komut bu nesneleri $Jobs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51476-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="51476-111">İkinci komut $Jobs dizisinin ilk üyesinin tüm akışı için derleme işi çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="51476-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="51476-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51476-112">PARAMETERS</span></span>

### <span data-ttu-id="51476-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="51476-113">-AutomationAccountName</span></span>
<span data-ttu-id="51476-114">DSC derleme işini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51476-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="51476-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51476-115">-DefaultProfile</span></span>
<span data-ttu-id="51476-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="51476-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51476-117">-ID</span><span class="sxs-lookup"><span data-stu-id="51476-117">-Id</span></span>
<span data-ttu-id="51476-118">Bu cmdlet 'in çıkışı aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="51476-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="51476-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51476-119">-ResourceGroupName</span></span>
<span data-ttu-id="51476-120">Bu cmdlet 'in akış kayıtlarını aldığı DSC derleme işini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51476-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="51476-121">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="51476-121">-StartTime</span></span>
<span data-ttu-id="51476-122">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51476-122">Specifies a start time.</span></span>
<span data-ttu-id="51476-123">Bu cmdlet, DSC derleme işinin bu süreden sonra aldığı akış kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="51476-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

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

### <span data-ttu-id="51476-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="51476-124">-Stream</span></span>
<span data-ttu-id="51476-125">Bu cmdlet 'in aldığı çıktı için akış türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="51476-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="51476-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="51476-126">Valid values are:</span></span> 
- <span data-ttu-id="51476-127">Tüm</span><span class="sxs-lookup"><span data-stu-id="51476-127">Any</span></span> 
- <span data-ttu-id="51476-128">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="51476-128">Warning</span></span> 
- <span data-ttu-id="51476-129">Hatalar</span><span class="sxs-lookup"><span data-stu-id="51476-129">Error</span></span> 
- <span data-ttu-id="51476-130">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="51476-130">Verbose</span></span>

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

### <span data-ttu-id="51476-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51476-131">CommonParameters</span></span>
<span data-ttu-id="51476-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51476-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51476-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51476-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51476-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51476-134">INPUTS</span></span>

### <span data-ttu-id="51476-135">System. Guid</span><span class="sxs-lookup"><span data-stu-id="51476-135">System.Guid</span></span>

### <span data-ttu-id="51476-136">Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="51476-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="51476-137">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="51476-137">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="51476-138">System. String</span><span class="sxs-lookup"><span data-stu-id="51476-138">System.String</span></span>

## <span data-ttu-id="51476-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51476-139">OUTPUTS</span></span>

### <span data-ttu-id="51476-140">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="51476-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="51476-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51476-141">NOTES</span></span>

## <span data-ttu-id="51476-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51476-142">RELATED LINKS</span></span>

[<span data-ttu-id="51476-143">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="51476-143">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="51476-144">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="51476-144">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


