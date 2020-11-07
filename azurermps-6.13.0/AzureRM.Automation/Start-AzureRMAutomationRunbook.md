---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46544d42cb28f5fca046586696b95286cdd7f3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763481"
---
# <span data-ttu-id="ba91a-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ba91a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba91a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba91a-103">Runbook işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba91a-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba91a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba91a-104">SYNTAX</span></span>

### <span data-ttu-id="ba91a-105">ByAsynchronousReturnJob (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba91a-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba91a-106">Bysynchronousreturnjoi koyun</span><span class="sxs-lookup"><span data-stu-id="ba91a-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba91a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba91a-107">DESCRIPTION</span></span>
<span data-ttu-id="ba91a-108">**Start-AzureRmAutomationRunbook** cmdlet 'ı bir Azure Otomasyonu runbook işini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba91a-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="ba91a-109">Runbook 'un KIMLIĞINI veya adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ba91a-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="ba91a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba91a-110">EXAMPLES</span></span>

### <span data-ttu-id="ba91a-111">Örnek 1: runbook işi başlatma</span><span class="sxs-lookup"><span data-stu-id="ba91a-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ba91a-112">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki Runbk01 adındaki runbook için bir runbook işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba91a-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="ba91a-113">Örnek 2: runbook işi başlatma ve sonuçları bekleme</span><span class="sxs-lookup"><span data-stu-id="ba91a-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="ba91a-114">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki Runbk01 adındaki runbook için bir runbook işi başlatır.</span><span class="sxs-lookup"><span data-stu-id="ba91a-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="ba91a-115">Bu komut, _wait_ parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba91a-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="ba91a-116">Bu nedenle, iş tamamlandıktan sonra sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba91a-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="ba91a-117">Bu cmdlet, sonuçlar için 1000 saniye kadar bekler.</span><span class="sxs-lookup"><span data-stu-id="ba91a-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="ba91a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba91a-118">PARAMETERS</span></span>

### <span data-ttu-id="ba91a-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba91a-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="ba91a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba91a-120">-DefaultProfile</span></span>
<span data-ttu-id="ba91a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba91a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba91a-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="ba91a-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="ba91a-123">Bu cmdlet 'in işi terk etmeden önce bitmesi için bekleyeceği saniye sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba91a-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="ba91a-124">Varsayılan değer 10800 veya üç saattir.</span><span class="sxs-lookup"><span data-stu-id="ba91a-124">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="ba91a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba91a-125">-Name</span></span>
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

### <span data-ttu-id="ba91a-126">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="ba91a-126">-Parameters</span></span>
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

### <span data-ttu-id="ba91a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba91a-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ba91a-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="ba91a-128">-RunOn</span></span>
<span data-ttu-id="ba91a-129">Runbook 'un çalıştırılacağı karma çalışanı grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba91a-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="ba91a-130">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="ba91a-130">-Wait</span></span>
<span data-ttu-id="ba91a-131">Bu cmdlet 'in işi tamamlamasını, askıya almayı veya başarısız olarak beklediğini gösterir ve ardından denetimi Azure PowerShell 'e döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba91a-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="ba91a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba91a-132">CommonParameters</span></span>
<span data-ttu-id="ba91a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba91a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba91a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba91a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba91a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba91a-135">INPUTS</span></span>

### <span data-ttu-id="ba91a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba91a-136">System.String</span></span>

## <span data-ttu-id="ba91a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba91a-137">OUTPUTS</span></span>

### <span data-ttu-id="ba91a-138">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="ba91a-138">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="ba91a-139">- _Wait_ parametresini belirtmediğiniz sürece, bu cmdlet bir **iş** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba91a-139">-This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>
<span data-ttu-id="ba91a-140">_Bekleme_ seçeneğini belirtmezseniz, Azure PowerShell, hemen bir **iş** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba91a-140">-If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="ba91a-141">- _Beklemeyi_ belirtirseniz, Azure PowerShell işi tamamlar ve sonucu verir.</span><span class="sxs-lookup"><span data-stu-id="ba91a-141">-If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="ba91a-142">-Sonuç bir **iş** nesnesi değil.</span><span class="sxs-lookup"><span data-stu-id="ba91a-142">-The result is not a **Job** object.</span></span>

### <span data-ttu-id="ba91a-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ba91a-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ba91a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba91a-144">NOTES</span></span>

## <span data-ttu-id="ba91a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba91a-145">RELATED LINKS</span></span>

[<span data-ttu-id="ba91a-146">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-148">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-149">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-150">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-151">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba91a-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba91a-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
