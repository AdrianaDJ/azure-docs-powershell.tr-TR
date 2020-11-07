---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: b0bebe0f831cc4041ecdeeeaa3ec8066faeacc8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761512"
---
# <span data-ttu-id="8036d-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8036d-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="8036d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8036d-102">SYNOPSIS</span></span>
<span data-ttu-id="8036d-103">Otomasyon hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8036d-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="8036d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8036d-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8036d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8036d-105">DESCRIPTION</span></span>
<span data-ttu-id="8036d-106">**Set-AzAutomationAccount** cmdlet 'ı bir Azure Otomasyonu hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8036d-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="8036d-107">Otomasyon hesapları hakkında daha fazla bilgi için New-AzAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="8036d-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8036d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8036d-108">EXAMPLES</span></span>

### <span data-ttu-id="8036d-109">Örnek 1: Otomasyon hesabının etiketlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8036d-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="8036d-110">İlk komut $Tags değişkenine iki anahtar/değer çifti atar.</span><span class="sxs-lookup"><span data-stu-id="8036d-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="8036d-111">İkinci komut, AutomationAccount01 adlı Otomasyon hesabı için $Tags etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8036d-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="8036d-112">Örnek 2: Otomasyon hesabı için planı değiştirme</span><span class="sxs-lookup"><span data-stu-id="8036d-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="8036d-113">Bu komut, AutomationAccount01 adlı Otomasyon hesabı için planı temel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8036d-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="8036d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8036d-114">PARAMETERS</span></span>

### <span data-ttu-id="8036d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8036d-115">-DefaultProfile</span></span>
<span data-ttu-id="8036d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8036d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8036d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8036d-117">-Name</span></span>
<span data-ttu-id="8036d-118">Bu cmdlet 'in değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8036d-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8036d-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="8036d-119">-Plan</span></span>
<span data-ttu-id="8036d-120">Otomasyon hesabı için planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8036d-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="8036d-121">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8036d-121">Valid values are:</span></span>
- <span data-ttu-id="8036d-122">Ana</span><span class="sxs-lookup"><span data-stu-id="8036d-122">Basic</span></span>
- <span data-ttu-id="8036d-123">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="8036d-123">Free</span></span>

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

### <span data-ttu-id="8036d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8036d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8036d-125">Bu cmdlet 'in değiştirdiği Otomasyon hesabını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8036d-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8036d-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="8036d-126">-Tags</span></span>
<span data-ttu-id="8036d-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8036d-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8036d-128">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8036d-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8036d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8036d-129">CommonParameters</span></span>
<span data-ttu-id="8036d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8036d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8036d-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8036d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8036d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8036d-132">INPUTS</span></span>

### <span data-ttu-id="8036d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8036d-133">System.String</span></span>

### <span data-ttu-id="8036d-134">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="8036d-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="8036d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8036d-135">OUTPUTS</span></span>

### <span data-ttu-id="8036d-136">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8036d-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8036d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8036d-137">NOTES</span></span>

## <span data-ttu-id="8036d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8036d-138">RELATED LINKS</span></span>

[<span data-ttu-id="8036d-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8036d-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="8036d-140">Yeni-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8036d-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="8036d-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8036d-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
