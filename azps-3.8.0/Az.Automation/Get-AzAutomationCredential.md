---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098191"
---
# <span data-ttu-id="a3fa2-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a3fa2-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="a3fa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fa2-103">Otomasyon kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="a3fa2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3fa2-104">SYNTAX</span></span>

### <span data-ttu-id="a3fa2-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3fa2-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3fa2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a3fa2-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3fa2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3fa2-107">DESCRIPTION</span></span>
<span data-ttu-id="a3fa2-108">**Get-AzAutomationCredential** cmdlet 'i bir veya daha fazla Azure Otomasyonu kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="a3fa2-109">Varsayılan olarak, tüm kimlik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="a3fa2-110">Belirli bir kimlik bilgisinin alınacağı kimlik bilgisinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="a3fa2-111">Güvenlik amaçları doğrultusunda bu cmdlet kimlik bilgileri parolalarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="a3fa2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3fa2-112">EXAMPLES</span></span>

### <span data-ttu-id="a3fa2-113">Örnek 1: tüm kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="a3fa2-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a3fa2-114">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm kimlik bilgilerinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a3fa2-115">Örnek 2: kimlik bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="a3fa2-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="a3fa2-116">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoCredential adlı kimlik bilgisinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a3fa2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3fa2-117">PARAMETERS</span></span>

### <span data-ttu-id="a3fa2-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a3fa2-118">-AutomationAccountName</span></span>
<span data-ttu-id="a3fa2-119">Bu cmdlet 'in kimlik bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="a3fa2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3fa2-120">-DefaultProfile</span></span>
<span data-ttu-id="a3fa2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a3fa2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3fa2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3fa2-122">-Name</span></span>
<span data-ttu-id="a3fa2-123">Alınacak kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3fa2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3fa2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3fa2-125">Bu cmdlet 'in kimlik bilgilerini aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="a3fa2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fa2-126">CommonParameters</span></span>
<span data-ttu-id="a3fa2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3fa2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fa2-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3fa2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fa2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3fa2-129">INPUTS</span></span>

### <span data-ttu-id="a3fa2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a3fa2-130">System.String</span></span>

## <span data-ttu-id="a3fa2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3fa2-131">OUTPUTS</span></span>

### <span data-ttu-id="a3fa2-132">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="a3fa2-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="a3fa2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3fa2-133">NOTES</span></span>

## <span data-ttu-id="a3fa2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3fa2-134">RELATED LINKS</span></span>

[<span data-ttu-id="a3fa2-135">Yeni-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a3fa2-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="a3fa2-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a3fa2-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="a3fa2-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a3fa2-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)

