---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: c7e4043cb6883020b8af15d13dd46c395997e116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595120"
---
# <span data-ttu-id="f3d9a-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f3d9a-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="f3d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d9a-103">Otomasyon 'daki DSC derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3d9a-104">SYNTAX</span></span>

### <span data-ttu-id="f3d9a-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3d9a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d9a-106">Byjobıd</span><span class="sxs-lookup"><span data-stu-id="f3d9a-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d9a-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f3d9a-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d9a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3d9a-108">DESCRIPTION</span></span>
<span data-ttu-id="f3d9a-109">**Get-AzureRmAutomationDscCompilationJob** cmdlet 'i, Mac OTOMASYONUNDA APS Istenen durum yapılandırma (DSC) derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="f3d9a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3d9a-110">EXAMPLES</span></span>

### <span data-ttu-id="f3d9a-111">Örnek 1: tüm DSC derleme işlerini al</span><span class="sxs-lookup"><span data-stu-id="f3d9a-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f3d9a-112">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3d9a-113">Örnek 2: bir yapılandırma için DSC derleme işlerini alma</span><span class="sxs-lookup"><span data-stu-id="f3d9a-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f3d9a-114">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoConfiguration adlı DSC yapılandırmasına yönelik tüm derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f3d9a-115">Örnek 3: belirli bir DSC derleme işi edinme</span><span class="sxs-lookup"><span data-stu-id="f3d9a-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="f3d9a-116">Bu komut, Contoso17 adlı Otomasyon hesabında belirtilen KIMLIĞE sahip derleme işini alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f3d9a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3d9a-117">PARAMETERS</span></span>

### <span data-ttu-id="f3d9a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3d9a-118">-AutomationAccountName</span></span>
<span data-ttu-id="f3d9a-119">Bu cmdlet 'in aldığı DSC derleme işlerini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3d9a-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f3d9a-120">-ConfigurationName</span></span>
<span data-ttu-id="f3d9a-121">Bu cmdlet 'in derleme işlerini aldığı DSC yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d9a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d9a-122">-DefaultProfile</span></span>
<span data-ttu-id="f3d9a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f3d9a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3d9a-124">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="f3d9a-124">-EndTime</span></span>
<span data-ttu-id="f3d9a-125">Bitiş saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-125">Specifies an end time.</span></span>
<span data-ttu-id="f3d9a-126">Bu cmdlet, bu parametrenin belirttiği zamana kadar başlatılan derleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d9a-127">-ID</span><span class="sxs-lookup"><span data-stu-id="f3d9a-127">-Id</span></span>
<span data-ttu-id="f3d9a-128">Bu cmdlet 'in aldığı DSC derleme işinin benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="f3d9a-130">Bu cmdlet 'in DSC derleme işlerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="f3d9a-131">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="f3d9a-131">-StartTime</span></span>
<span data-ttu-id="f3d9a-132">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-132">Specifies a start time.</span></span>
<span data-ttu-id="f3d9a-133">Bu cmdlet, bu parametrenin belirttiği zamandan sonraki veya sonraki işleri alır.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d9a-134">-Durum</span><span class="sxs-lookup"><span data-stu-id="f3d9a-134">-Status</span></span>
<span data-ttu-id="f3d9a-135">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f3d9a-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f3d9a-136">Valid values are:</span></span> 

- <span data-ttu-id="f3d9a-137">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="f3d9a-137">Completed</span></span> 
- <span data-ttu-id="f3d9a-138">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="f3d9a-138">Failed</span></span> 
- <span data-ttu-id="f3d9a-139">Sıradan</span><span class="sxs-lookup"><span data-stu-id="f3d9a-139">Queued</span></span> 
- <span data-ttu-id="f3d9a-140">Başlarken</span><span class="sxs-lookup"><span data-stu-id="f3d9a-140">Starting</span></span> 
- <span data-ttu-id="f3d9a-141">İlirken</span><span class="sxs-lookup"><span data-stu-id="f3d9a-141">Resuming</span></span> 
- <span data-ttu-id="f3d9a-142">Çalışması</span><span class="sxs-lookup"><span data-stu-id="f3d9a-142">Running</span></span> 
- <span data-ttu-id="f3d9a-143">Sahiptir</span><span class="sxs-lookup"><span data-stu-id="f3d9a-143">Stopped</span></span> 
- <span data-ttu-id="f3d9a-144">Arak</span><span class="sxs-lookup"><span data-stu-id="f3d9a-144">Stopping</span></span> 
- <span data-ttu-id="f3d9a-145">Etsin</span><span class="sxs-lookup"><span data-stu-id="f3d9a-145">Suspended</span></span> 
- <span data-ttu-id="f3d9a-146">Et</span><span class="sxs-lookup"><span data-stu-id="f3d9a-146">Suspending</span></span> 
- <span data-ttu-id="f3d9a-147">Etkinleştirirken</span><span class="sxs-lookup"><span data-stu-id="f3d9a-147">Activating</span></span>
- <span data-ttu-id="f3d9a-148">Yeni</span><span class="sxs-lookup"><span data-stu-id="f3d9a-148">New</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d9a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d9a-149">CommonParameters</span></span>
<span data-ttu-id="f3d9a-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d9a-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d9a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d9a-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3d9a-152">INPUTS</span></span>

### <span data-ttu-id="f3d9a-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f3d9a-153">None</span></span>
<span data-ttu-id="f3d9a-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f3d9a-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f3d9a-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3d9a-155">OUTPUTS</span></span>

### <span data-ttu-id="f3d9a-156">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="f3d9a-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="f3d9a-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3d9a-157">NOTES</span></span>

## <span data-ttu-id="f3d9a-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3d9a-158">RELATED LINKS</span></span>

[<span data-ttu-id="f3d9a-159">Get-Azurermautomationdsccompilationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="f3d9a-159">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="f3d9a-160">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f3d9a-160">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


