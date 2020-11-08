---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098196"
---
# <span data-ttu-id="beee9-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="beee9-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="beee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beee9-102">SYNOPSIS</span></span>
<span data-ttu-id="beee9-103">Kaynak grubundaki Otomasyon hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="beee9-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="beee9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="beee9-104">SYNTAX</span></span>

### <span data-ttu-id="beee9-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="beee9-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="beee9-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="beee9-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="beee9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="beee9-107">DESCRIPTION</span></span>
<span data-ttu-id="beee9-108">**Get-AzAutomationAccount** cmdlet 'i, kaynak grubundaki Azure Otomasyonu hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="beee9-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="beee9-109">Otomasyon hesapları hakkında daha fazla bilgi için New-AzAutomationAccount cmdlet bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="beee9-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="beee9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="beee9-110">EXAMPLES</span></span>

### <span data-ttu-id="beee9-111">Örnek 1: tüm hesapları alma</span><span class="sxs-lookup"><span data-stu-id="beee9-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="beee9-112">Bu komut, ResourceGroup03 adlı kaynak grubundaki tüm otomasyon hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="beee9-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="beee9-113">Örnek 2: hesap alma</span><span class="sxs-lookup"><span data-stu-id="beee9-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="beee9-114">Bu komut, ContosoResourceGroup adlı kaynak grubundaki ContosoAutomationAccount adlı Otomasyon hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="beee9-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="beee9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="beee9-115">PARAMETERS</span></span>

### <span data-ttu-id="beee9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beee9-116">-DefaultProfile</span></span>
<span data-ttu-id="beee9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="beee9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="beee9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="beee9-118">-Name</span></span>
<span data-ttu-id="beee9-119">Bu cmdlet 'in aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee9-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beee9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beee9-120">-ResourceGroupName</span></span>
<span data-ttu-id="beee9-121">Bu cmdlet 'in Otomasyon hesaplarını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="beee9-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beee9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beee9-122">CommonParameters</span></span>
<span data-ttu-id="beee9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="beee9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beee9-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beee9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beee9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="beee9-125">INPUTS</span></span>

### <span data-ttu-id="beee9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="beee9-126">System.String</span></span>

## <span data-ttu-id="beee9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="beee9-127">OUTPUTS</span></span>

### <span data-ttu-id="beee9-128">Microsoft. Azure. Commands. Automation. model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="beee9-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="beee9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="beee9-129">NOTES</span></span>

## <span data-ttu-id="beee9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="beee9-130">RELATED LINKS</span></span>

[<span data-ttu-id="beee9-131">Yeni-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="beee9-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="beee9-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="beee9-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="beee9-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="beee9-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


