---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765113"
---
# <span data-ttu-id="ee863-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="ee863-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="ee863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee863-102">SYNOPSIS</span></span>
<span data-ttu-id="ee863-103">DSC düğümünden otomatikleştirme 'ye gönderilen raporları alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee863-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee863-104">SYNTAX</span></span>

### <span data-ttu-id="ee863-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee863-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee863-106">En son</span><span class="sxs-lookup"><span data-stu-id="ee863-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee863-107">Byıd</span><span class="sxs-lookup"><span data-stu-id="ee863-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee863-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee863-108">DESCRIPTION</span></span>
<span data-ttu-id="ee863-109">**Get-AzureRmAutomationDscNodeReport** cmdlet 'ı, APS Istenen durum YAPıLANDıRMASı (DSC) düğümünden Azure Otomasyonu 'na gönderilen raporları alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="ee863-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee863-110">EXAMPLES</span></span>

### <span data-ttu-id="ee863-111">Örnek 1: DSC düğümü için tüm raporları alma</span><span class="sxs-lookup"><span data-stu-id="ee863-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="ee863-112">İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ee863-113">Komut bu nesneyi $Node değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ee863-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="ee863-114">İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen tüm raporlarda meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="ee863-115">Komut, düğümü $Node nesnesinin **ID** özelliğini kullanarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="ee863-116">Örnek 2: rapor KIMLIĞIYLE bir DSC düğümü için rapor alma</span><span class="sxs-lookup"><span data-stu-id="ee863-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="ee863-117">İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ee863-118">Komut bu nesneyi $Node değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ee863-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="ee863-119">İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen belirtilen KIMLIğIN meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ee863-120">Örnek 3: DSC düğümü için en son raporu alma</span><span class="sxs-lookup"><span data-stu-id="ee863-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="ee863-121">İlk komut, Contoso17 adlı Otomasyon hesabındaki Computer14 adındaki bilgisayar için DSC düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="ee863-122">Komut bu nesneyi $Node değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ee863-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="ee863-123">İkinci komut, Computer14 adlı DSC düğümünden Contoso17 adlı Otomasyon hesabına gönderilen en son raporun meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ee863-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee863-124">PARAMETERS</span></span>

### <span data-ttu-id="ee863-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee863-125">-AutomationAccountName</span></span>
<span data-ttu-id="ee863-126">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="ee863-127">Bu cmdlet, bu parametrenin belirttiği hesaba ait bir DSC düğümünün raporlarını dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="ee863-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="ee863-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee863-128">-DefaultProfile</span></span>
<span data-ttu-id="ee863-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee863-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee863-130">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="ee863-130">-EndTime</span></span>
<span data-ttu-id="ee863-131">Bitiş saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-131">Specifies an end time.</span></span>
<span data-ttu-id="ee863-132">Bu cmdlet, bu tarihten önce Otomasyon tarafından alınan raporları alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee863-133">-ID</span><span class="sxs-lookup"><span data-stu-id="ee863-133">-Id</span></span>
<span data-ttu-id="ee863-134">Bu cmdlet 'in alınacağı DSC düğümü raporunun benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee863-135">-En son</span><span class="sxs-lookup"><span data-stu-id="ee863-135">-Latest</span></span>
<span data-ttu-id="ee863-136">Bu cmdlet 'in yalnızca belirtilen düğüm için en son DSC raporunu aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee863-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee863-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="ee863-137">-NodeId</span></span>
<span data-ttu-id="ee863-138">Bu cmdlet 'in raporları aldığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee863-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee863-139">-ResourceGroupName</span></span>
<span data-ttu-id="ee863-140">Bu cmdlet 'in raporları aldığı DSC düğümünü içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="ee863-141">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ee863-141">-StartTime</span></span>
<span data-ttu-id="ee863-142">Başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee863-142">Specifies a start time.</span></span>
<span data-ttu-id="ee863-143">Bu cmdlet, bu süreden sonra Otomasyon tarafından alınan raporları alır.</span><span class="sxs-lookup"><span data-stu-id="ee863-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee863-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee863-144">CommonParameters</span></span>
<span data-ttu-id="ee863-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee863-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee863-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee863-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee863-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee863-147">INPUTS</span></span>

### <span data-ttu-id="ee863-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ee863-148">None</span></span>
<span data-ttu-id="ee863-149">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ee863-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee863-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee863-150">OUTPUTS</span></span>

### <span data-ttu-id="ee863-151">Microsoft. Azure. Commands. Automation. model. DscNode</span><span class="sxs-lookup"><span data-stu-id="ee863-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="ee863-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee863-152">NOTES</span></span>

## <span data-ttu-id="ee863-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee863-153">RELATED LINKS</span></span>

[<span data-ttu-id="ee863-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ee863-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="ee863-155">Dışarı aktarma-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="ee863-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

