---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 7a0341221dee0f282508377d1233e30deae1fcee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761988"
---
# <span data-ttu-id="162a8-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="162a8-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="162a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="162a8-102">SYNOPSIS</span></span>
<span data-ttu-id="162a8-103">Otomasyon hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="162a8-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="162a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="162a8-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="162a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="162a8-105">DESCRIPTION</span></span>
<span data-ttu-id="162a8-106">**Set-AzureRmAutomationAccount** cmdlet 'ı bir Azure Otomasyonu hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="162a8-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="162a8-107">Otomasyon hesapları hakkında daha fazla bilgi için New-AzureRmAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="162a8-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="162a8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="162a8-108">EXAMPLES</span></span>

### <span data-ttu-id="162a8-109">Örnek 1: Otomasyon hesabının etiketlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="162a8-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="162a8-110">İlk komut $Tags değişkenine iki anahtar/değer çifti atar.</span><span class="sxs-lookup"><span data-stu-id="162a8-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="162a8-111">İkinci komut, AutomationAccount01 adlı Otomasyon hesabı için $Tags etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="162a8-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="162a8-112">Örnek 2: Otomasyon hesabı için planı değiştirme</span><span class="sxs-lookup"><span data-stu-id="162a8-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="162a8-113">Bu komut, AutomationAccount01 adlı Otomasyon hesabı için planı temel olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="162a8-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="162a8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="162a8-114">PARAMETERS</span></span>

### <span data-ttu-id="162a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162a8-115">-DefaultProfile</span></span>
<span data-ttu-id="162a8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="162a8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="162a8-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="162a8-117">-Name</span></span>
<span data-ttu-id="162a8-118">Bu cmdlet 'in değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="162a8-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="162a8-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="162a8-119">-Plan</span></span>
<span data-ttu-id="162a8-120">Otomasyon hesabı için planı belirtir.</span><span class="sxs-lookup"><span data-stu-id="162a8-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="162a8-121">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="162a8-121">Valid values are:</span></span>
- <span data-ttu-id="162a8-122">Ana</span><span class="sxs-lookup"><span data-stu-id="162a8-122">Basic</span></span>
- <span data-ttu-id="162a8-123">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="162a8-123">Free</span></span>

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

### <span data-ttu-id="162a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="162a8-125">Bu cmdlet 'in değiştirdiği Otomasyon hesabını içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="162a8-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="162a8-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="162a8-126">-Tags</span></span>
<span data-ttu-id="162a8-127">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="162a8-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="162a8-128">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="162a8-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="162a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162a8-129">CommonParameters</span></span>
<span data-ttu-id="162a8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="162a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162a8-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="162a8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162a8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="162a8-132">INPUTS</span></span>

### <span data-ttu-id="162a8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="162a8-133">System.String</span></span>

### <span data-ttu-id="162a8-134">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="162a8-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="162a8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="162a8-135">OUTPUTS</span></span>

### <span data-ttu-id="162a8-136">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="162a8-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="162a8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="162a8-137">NOTES</span></span>

## <span data-ttu-id="162a8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="162a8-138">RELATED LINKS</span></span>

[<span data-ttu-id="162a8-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="162a8-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="162a8-140">Yeni-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="162a8-140">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="162a8-141">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="162a8-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
