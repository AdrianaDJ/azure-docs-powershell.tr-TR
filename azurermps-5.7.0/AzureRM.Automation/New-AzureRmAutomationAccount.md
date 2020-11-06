---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587710"
---
# <span data-ttu-id="34f0f-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34f0f-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="34f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="34f0f-103">Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34f0f-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34f0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34f0f-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f0f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="34f0f-106">**Yeni-AzureRmAutomationAccount** cmdlet 'i bir kaynak grubunda Azure Otomasyonu hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34f0f-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="34f0f-107">Otomasyon hesabı, diğer otomasyon hesaplarının kaynaklarından yalıtılmış olan otomasyon kaynakları için bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="34f0f-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="34f0f-108">Otomasyon kaynakları, runbook, Istenen durum yapılandırması (DSC) yapılandırmalarını, işlerini ve varlıklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="34f0f-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="34f0f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34f0f-109">EXAMPLES</span></span>

### <span data-ttu-id="34f0f-110">Örnek 1: Otomasyon hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="34f0f-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="34f0f-111">Bu komut, Doğu ABD bölgesinde ContosoAutomationAccount adlı yeni bir Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="34f0f-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="34f0f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34f0f-112">PARAMETERS</span></span>

### <span data-ttu-id="34f0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f0f-113">-DefaultProfile</span></span>
<span data-ttu-id="34f0f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="34f0f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34f0f-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="34f0f-115">-Location</span></span>
<span data-ttu-id="34f0f-116">Bu cmdlet 'in Otomasyon hesabını oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f0f-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="34f0f-117">Geçerli konumları almak için Get-AzureRMLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="34f0f-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f0f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="34f0f-118">-Name</span></span>
<span data-ttu-id="34f0f-119">Otomasyon hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f0f-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f0f-120">-Plan</span><span class="sxs-lookup"><span data-stu-id="34f0f-120">-Plan</span></span>
<span data-ttu-id="34f0f-121">Otomasyon hesabı için planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f0f-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="34f0f-122">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="34f0f-122">Valid values are:</span></span>

- <span data-ttu-id="34f0f-123">Ana</span><span class="sxs-lookup"><span data-stu-id="34f0f-123">Basic</span></span>
- <span data-ttu-id="34f0f-124">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="34f0f-124">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f0f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f0f-125">-ResourceGroupName</span></span>
<span data-ttu-id="34f0f-126">Bu cmdlet 'in Otomasyon hesabı eklediği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f0f-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="34f0f-127">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="34f0f-127">-Tags</span></span>
<span data-ttu-id="34f0f-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="34f0f-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34f0f-129">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="34f0f-129">For example:</span></span>

<span data-ttu-id="34f0f-130">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="34f0f-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34f0f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f0f-131">CommonParameters</span></span>
<span data-ttu-id="34f0f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34f0f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f0f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f0f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f0f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34f0f-134">INPUTS</span></span>

### <span data-ttu-id="34f0f-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34f0f-135">None</span></span>
<span data-ttu-id="34f0f-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="34f0f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34f0f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34f0f-137">OUTPUTS</span></span>

### <span data-ttu-id="34f0f-138">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34f0f-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="34f0f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34f0f-139">NOTES</span></span>

## <span data-ttu-id="34f0f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34f0f-140">RELATED LINKS</span></span>

[<span data-ttu-id="34f0f-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34f0f-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="34f0f-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34f0f-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="34f0f-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="34f0f-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
