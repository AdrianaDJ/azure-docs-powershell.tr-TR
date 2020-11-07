---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753283"
---
# <span data-ttu-id="d8d11-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d8d11-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="d8d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d11-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d11-103">Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d11-103">Creates an Automation account.</span></span>

## <span data-ttu-id="d8d11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8d11-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d11-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8d11-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d11-106">**New-AzAutomationAccount** cmdlet 'i bir kaynak grubunda Azure Otomasyonu hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d11-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="d8d11-107">Otomasyon hesabı, diğer otomasyon hesaplarının kaynaklarından yalıtılmış olan otomasyon kaynakları için bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="d8d11-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="d8d11-108">Otomasyon kaynakları, runbook, Istenen durum yapılandırması (DSC) yapılandırmalarını, işlerini ve varlıklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="d8d11-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="d8d11-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8d11-109">EXAMPLES</span></span>

### <span data-ttu-id="d8d11-110">Örnek 1: Otomasyon hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8d11-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8d11-111">Bu komut, Doğu ABD bölgesinde ContosoAutomationAccount adlı yeni bir Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8d11-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="d8d11-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8d11-112">PARAMETERS</span></span>

### <span data-ttu-id="d8d11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d11-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d11-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d8d11-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8d11-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="d8d11-115">-Location</span></span>
<span data-ttu-id="d8d11-116">Bu cmdlet 'in Otomasyon hesabını oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8d11-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="d8d11-117">Geçerli konumları almak için Get-AzLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d8d11-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d11-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8d11-118">-Name</span></span>
<span data-ttu-id="d8d11-119">Otomasyon hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8d11-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d11-120">-Plan</span><span class="sxs-lookup"><span data-stu-id="d8d11-120">-Plan</span></span>
<span data-ttu-id="d8d11-121">Otomasyon hesabı için planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8d11-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="d8d11-122">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="d8d11-122">Valid values are:</span></span>
- <span data-ttu-id="d8d11-123">Ana</span><span class="sxs-lookup"><span data-stu-id="d8d11-123">Basic</span></span>
- <span data-ttu-id="d8d11-124">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="d8d11-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d11-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d11-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8d11-126">Bu cmdlet 'in Otomasyon hesabı eklediği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8d11-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="d8d11-127">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="d8d11-127">-Tags</span></span>
<span data-ttu-id="d8d11-128">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="d8d11-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d8d11-129">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="d8d11-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d11-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d11-130">CommonParameters</span></span>
<span data-ttu-id="d8d11-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8d11-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d11-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d11-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d11-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8d11-133">INPUTS</span></span>

### <span data-ttu-id="d8d11-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d8d11-134">System.String</span></span>

### <span data-ttu-id="d8d11-135">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="d8d11-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="d8d11-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8d11-136">OUTPUTS</span></span>

### <span data-ttu-id="d8d11-137">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d8d11-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="d8d11-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8d11-138">NOTES</span></span>

## <span data-ttu-id="d8d11-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8d11-139">RELATED LINKS</span></span>

[<span data-ttu-id="d8d11-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d8d11-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="d8d11-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d8d11-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="d8d11-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d8d11-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
