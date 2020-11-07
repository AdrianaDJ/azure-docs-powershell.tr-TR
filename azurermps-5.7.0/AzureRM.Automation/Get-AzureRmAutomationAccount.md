---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765122"
---
# <span data-ttu-id="12f46-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12f46-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="12f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12f46-102">SYNOPSIS</span></span>
<span data-ttu-id="12f46-103">Kaynak grubundaki Otomasyon hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="12f46-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12f46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12f46-104">SYNTAX</span></span>

### <span data-ttu-id="12f46-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12f46-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12f46-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="12f46-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f46-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12f46-107">DESCRIPTION</span></span>
<span data-ttu-id="12f46-108">**Get-AzureRmAutomationAccount** cmdlet 'i, kaynak grubundaki Azure Otomasyonu hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="12f46-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="12f46-109">Otomasyon hesapları hakkında daha fazla bilgi için New-AzureRmAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="12f46-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="12f46-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12f46-110">EXAMPLES</span></span>

### <span data-ttu-id="12f46-111">Örnek 1: tüm hesapları alma</span><span class="sxs-lookup"><span data-stu-id="12f46-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="12f46-112">Bu komut, ResourceGroup03 adlı kaynak grubundaki tüm otomasyon hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="12f46-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="12f46-113">Örnek 2: hesap alma</span><span class="sxs-lookup"><span data-stu-id="12f46-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="12f46-114">Bu komut, ContosoResourceGroup adlı kaynak grubundaki ContosoAutomationAccount adlı Otomasyon hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="12f46-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="12f46-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12f46-115">PARAMETERS</span></span>

### <span data-ttu-id="12f46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f46-116">-DefaultProfile</span></span>
<span data-ttu-id="12f46-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="12f46-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12f46-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="12f46-118">-Name</span></span>
<span data-ttu-id="12f46-119">Bu cmdlet 'in aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f46-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f46-120">-ResourceGroupName</span></span>
<span data-ttu-id="12f46-121">Bu cmdlet 'in Otomasyon hesaplarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12f46-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f46-122">CommonParameters</span></span>
<span data-ttu-id="12f46-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12f46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f46-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f46-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f46-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12f46-125">INPUTS</span></span>

### <span data-ttu-id="12f46-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="12f46-126">None</span></span>
<span data-ttu-id="12f46-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="12f46-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12f46-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12f46-128">OUTPUTS</span></span>

### <span data-ttu-id="12f46-129">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12f46-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="12f46-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12f46-130">NOTES</span></span>

## <span data-ttu-id="12f46-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12f46-131">RELATED LINKS</span></span>

[<span data-ttu-id="12f46-132">Yeni-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12f46-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="12f46-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12f46-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="12f46-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="12f46-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


