---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762884"
---
# <span data-ttu-id="8cc42-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8cc42-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="8cc42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc42-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc42-103">Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cc42-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cc42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8cc42-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cc42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8cc42-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc42-106">**Yeni-AzureRmAutomationAccount** cmdlet 'i bir kaynak grubunda Azure Otomasyonu hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cc42-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="8cc42-107">Otomasyon hesabı, diğer otomasyon hesaplarının kaynaklarından yalıtılmış olan otomasyon kaynakları için bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="8cc42-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="8cc42-108">Otomasyon kaynakları, runbook, Istenen durum yapılandırması (DSC) yapılandırmalarını, işlerini ve varlıklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="8cc42-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="8cc42-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8cc42-109">EXAMPLES</span></span>

### <span data-ttu-id="8cc42-110">Örnek 1: Otomasyon hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8cc42-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8cc42-111">Bu komut, Doğu ABD bölgesinde ContosoAutomationAccount adlı yeni bir Otomasyon hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cc42-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="8cc42-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8cc42-112">PARAMETERS</span></span>

### <span data-ttu-id="8cc42-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="8cc42-113">-Location</span></span>
<span data-ttu-id="8cc42-114">Bu cmdlet 'in Otomasyon hesabını oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cc42-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="8cc42-115">Geçerli konumları almak için Get-AzureRMLocation cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8cc42-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="8cc42-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8cc42-116">-Name</span></span>
<span data-ttu-id="8cc42-117">Otomasyon hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cc42-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="8cc42-118">-Plan</span><span class="sxs-lookup"><span data-stu-id="8cc42-118">-Plan</span></span>
<span data-ttu-id="8cc42-119">Otomasyon hesabı için planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cc42-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="8cc42-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8cc42-120">Valid values are:</span></span>

- <span data-ttu-id="8cc42-121">Ana</span><span class="sxs-lookup"><span data-stu-id="8cc42-121">Basic</span></span>
- <span data-ttu-id="8cc42-122">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="8cc42-122">Free</span></span>

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

### <span data-ttu-id="8cc42-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc42-123">-ResourceGroupName</span></span>
<span data-ttu-id="8cc42-124">Bu cmdlet 'in Otomasyon hesabı eklediği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8cc42-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="8cc42-125">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="8cc42-125">-Tags</span></span>
<span data-ttu-id="8cc42-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8cc42-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8cc42-127">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8cc42-127">For example:</span></span>

<span data-ttu-id="8cc42-128">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8cc42-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8cc42-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc42-129">-DefaultProfile</span></span>
<span data-ttu-id="8cc42-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8cc42-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cc42-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc42-131">CommonParameters</span></span>
<span data-ttu-id="8cc42-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8cc42-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc42-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc42-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc42-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8cc42-134">INPUTS</span></span>

## <span data-ttu-id="8cc42-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8cc42-135">OUTPUTS</span></span>

### <span data-ttu-id="8cc42-136">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8cc42-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8cc42-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8cc42-137">NOTES</span></span>

## <span data-ttu-id="8cc42-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8cc42-138">RELATED LINKS</span></span>

[<span data-ttu-id="8cc42-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8cc42-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="8cc42-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8cc42-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="8cc42-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8cc42-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
