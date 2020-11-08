---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096048"
---
# <span data-ttu-id="0c786-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="0c786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c786-102">SYNOPSIS</span></span>
<span data-ttu-id="0c786-103">Runbook işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="0c786-103">Starts a runbook job.</span></span>

## <span data-ttu-id="0c786-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c786-104">SYNTAX</span></span>

### <span data-ttu-id="0c786-105">ByAsynchronousReturnJob (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c786-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c786-106">Bysynchronousreturnjoi koyun</span><span class="sxs-lookup"><span data-stu-id="0c786-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c786-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c786-107">DESCRIPTION</span></span>
<span data-ttu-id="0c786-108">**Start-AzAutomationRunbook** cmdlet 'ı bir Azure Otomasyonu runbook işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="0c786-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="0c786-109">Runbook 'un KIMLIĞINI veya adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c786-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="0c786-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c786-110">EXAMPLES</span></span>

### <span data-ttu-id="0c786-111">Örnek 1: runbook işi başlatma</span><span class="sxs-lookup"><span data-stu-id="0c786-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0c786-112">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki Runbk01 adındaki runbook için bir runbook işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0c786-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="0c786-113">Örnek 2: parametrelerle bir Python 2 runbook işi başlatma</span><span class="sxs-lookup"><span data-stu-id="0c786-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="0c786-114">Bu komut, RunbkPy01 adlı Azure Otomasyonu hesabındaki Contoso17 adlı Azure Automation hesabındaki adlı bir runbook işini ilk Konumsal parametre ve ikinci bir "ValueForPosition2" olarak başlatır.</span><span class="sxs-lookup"><span data-stu-id="0c786-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="0c786-115">Örnek 3: runbook işi başlatma ve sonuçları bekleme</span><span class="sxs-lookup"><span data-stu-id="0c786-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="0c786-116">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki Runbk01 adındaki runbook için bir runbook işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="0c786-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="0c786-117">Bu komut, _wait_ parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c786-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="0c786-118">Bu nedenle, iş tamamlandıktan sonra sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c786-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="0c786-119">Bu cmdlet, sonuçlar için 1000 saniye kadar bekler.</span><span class="sxs-lookup"><span data-stu-id="0c786-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="0c786-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c786-120">PARAMETERS</span></span>

### <span data-ttu-id="0c786-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c786-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="0c786-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c786-122">-DefaultProfile</span></span>
<span data-ttu-id="0c786-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0c786-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c786-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="0c786-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="0c786-125">Bu cmdlet 'in işi terk etmeden önce bitmesi için bekleyeceği saniye sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c786-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="0c786-126">Varsayılan değer 10800 veya üç saattir.</span><span class="sxs-lookup"><span data-stu-id="0c786-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c786-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c786-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c786-128">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="0c786-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c786-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c786-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0c786-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="0c786-130">-RunOn</span></span>
<span data-ttu-id="0c786-131">Runbook 'un çalıştırılacağı karma çalışanı grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c786-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c786-132">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="0c786-132">-Wait</span></span>
<span data-ttu-id="0c786-133">Bu cmdlet 'in işi tamamlamasını, askıya almayı veya başarısız olarak beklediğini gösterir ve ardından denetimi Azure PowerShell 'e döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c786-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c786-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c786-134">CommonParameters</span></span>
<span data-ttu-id="0c786-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c786-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c786-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c786-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c786-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c786-137">INPUTS</span></span>

### <span data-ttu-id="0c786-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0c786-138">System.String</span></span>

## <span data-ttu-id="0c786-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c786-139">OUTPUTS</span></span>

### <span data-ttu-id="0c786-140">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="0c786-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="0c786-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0c786-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0c786-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c786-142">NOTES</span></span>

## <span data-ttu-id="0c786-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c786-143">RELATED LINKS</span></span>

[<span data-ttu-id="0c786-144">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-147">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-148">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-149">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="0c786-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0c786-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
