---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109220"
---
# <span data-ttu-id="ef5b7-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ef5b7-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="ef5b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5b7-103">Otomasyon 'daki DSC derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="ef5b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef5b7-104">SYNTAX</span></span>

### <span data-ttu-id="ef5b7-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef5b7-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef5b7-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="ef5b7-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef5b7-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ef5b7-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef5b7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef5b7-108">DESCRIPTION</span></span>
<span data-ttu-id="ef5b7-109">**Get-AzAutomationDscCompilationJob** cmdlet 'i, iş,</span><span class="sxs-lookup"><span data-stu-id="ef5b7-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="ef5b7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef5b7-110">EXAMPLES</span></span>

### <span data-ttu-id="ef5b7-111">Örnek 1: tüm DSC derleme işlerini al</span><span class="sxs-lookup"><span data-stu-id="ef5b7-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ef5b7-112">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ef5b7-113">Örnek 2: bir yapılandırma için DSC derleme işlerini alma</span><span class="sxs-lookup"><span data-stu-id="ef5b7-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="ef5b7-114">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConfiguration adlı DSC yapılandırmasına yönelik tüm derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ef5b7-115">Örnek 3: belirli bir DSC derleme işi edinme</span><span class="sxs-lookup"><span data-stu-id="ef5b7-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="ef5b7-116">Bu komut, Contoso17 adlı Otomasyon hesabında belirtilen KIMLIĞE sahip derleme işini alır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ef5b7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef5b7-117">PARAMETERS</span></span>

### <span data-ttu-id="ef5b7-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef5b7-118">-AutomationAccountName</span></span>
<span data-ttu-id="ef5b7-119">Bu cmdlet 'in aldığı DSC derleme işlerini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ef5b7-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ef5b7-120">-ConfigurationName</span></span>
<span data-ttu-id="ef5b7-121">Bu cmdlet 'in derleme işlerini aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5b7-122">-DefaultProfile</span></span>
<span data-ttu-id="ef5b7-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ef5b7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef5b7-124">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="ef5b7-124">-EndTime</span></span>
<span data-ttu-id="ef5b7-125">Bitiş saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-125">Specifies an end time.</span></span>
<span data-ttu-id="ef5b7-126">Bu cmdlet, bu parametrenin belirttiği zamana kadar başlatılan derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b7-127">-ID</span><span class="sxs-lookup"><span data-stu-id="ef5b7-127">-Id</span></span>
<span data-ttu-id="ef5b7-128">Bu cmdlet 'in aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5b7-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef5b7-130">Bu cmdlet 'in DSC derleme işlerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="ef5b7-131">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ef5b7-131">-StartTime</span></span>
<span data-ttu-id="ef5b7-132">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-132">Specifies a start time.</span></span>
<span data-ttu-id="ef5b7-133">Bu cmdlet, bu parametrenin belirttiği zamandan sonraki veya sonraki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b7-134">-Durum</span><span class="sxs-lookup"><span data-stu-id="ef5b7-134">-Status</span></span>
<span data-ttu-id="ef5b7-135">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ef5b7-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ef5b7-136">Valid values are:</span></span> 
- <span data-ttu-id="ef5b7-137">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="ef5b7-137">Completed</span></span> 
- <span data-ttu-id="ef5b7-138">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="ef5b7-138">Failed</span></span> 
- <span data-ttu-id="ef5b7-139">Sıradan</span><span class="sxs-lookup"><span data-stu-id="ef5b7-139">Queued</span></span> 
- <span data-ttu-id="ef5b7-140">Başlarken</span><span class="sxs-lookup"><span data-stu-id="ef5b7-140">Starting</span></span> 
- <span data-ttu-id="ef5b7-141">İlirken</span><span class="sxs-lookup"><span data-stu-id="ef5b7-141">Resuming</span></span> 
- <span data-ttu-id="ef5b7-142">Çalışması</span><span class="sxs-lookup"><span data-stu-id="ef5b7-142">Running</span></span> 
- <span data-ttu-id="ef5b7-143">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="ef5b7-143">Stopped</span></span> 
- <span data-ttu-id="ef5b7-144">Arak</span><span class="sxs-lookup"><span data-stu-id="ef5b7-144">Stopping</span></span> 
- <span data-ttu-id="ef5b7-145">Etsin</span><span class="sxs-lookup"><span data-stu-id="ef5b7-145">Suspended</span></span> 
- <span data-ttu-id="ef5b7-146">Et</span><span class="sxs-lookup"><span data-stu-id="ef5b7-146">Suspending</span></span> 
- <span data-ttu-id="ef5b7-147">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="ef5b7-147">Activating</span></span>
- <span data-ttu-id="ef5b7-148">Yeni</span><span class="sxs-lookup"><span data-stu-id="ef5b7-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5b7-149">CommonParameters</span></span>
<span data-ttu-id="ef5b7-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef5b7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5b7-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5b7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5b7-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef5b7-152">INPUTS</span></span>

### <span data-ttu-id="ef5b7-153">System. Guid</span><span class="sxs-lookup"><span data-stu-id="ef5b7-153">System.Guid</span></span>

### <span data-ttu-id="ef5b7-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ef5b7-154">System.String</span></span>

## <span data-ttu-id="ef5b7-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef5b7-155">OUTPUTS</span></span>

### <span data-ttu-id="ef5b7-156">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="ef5b7-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="ef5b7-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef5b7-157">NOTES</span></span>

## <span data-ttu-id="ef5b7-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef5b7-158">RELATED LINKS</span></span>

[<span data-ttu-id="ef5b7-159">Get-Azautomationdsccompilationjoi Input</span><span class="sxs-lookup"><span data-stu-id="ef5b7-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="ef5b7-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ef5b7-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


