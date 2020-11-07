---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753343"
---
# <span data-ttu-id="37dcc-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="37dcc-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="37dcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="37dcc-103">Otomasyon kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="37dcc-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="37dcc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37dcc-104">SYNTAX</span></span>

### <span data-ttu-id="37dcc-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37dcc-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37dcc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="37dcc-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37dcc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="37dcc-107">DESCRIPTION</span></span>
<span data-ttu-id="37dcc-108">**Get-AzAutomationCredential** cmdlet 'i bir veya daha fazla Azure Otomasyonu kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="37dcc-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="37dcc-109">Varsayılan olarak, tüm kimlik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="37dcc-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="37dcc-110">Belirli bir kimlik bilgisinin alınacağı kimlik bilgisinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="37dcc-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="37dcc-111">Güvenlik amaçları doğrultusunda bu cmdlet kimlik bilgileri parolalarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="37dcc-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="37dcc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37dcc-112">EXAMPLES</span></span>

### <span data-ttu-id="37dcc-113">Örnek 1: tüm kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="37dcc-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="37dcc-114">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm kimlik bilgilerinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="37dcc-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="37dcc-115">Örnek 2: kimlik bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="37dcc-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="37dcc-116">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoCredential adlı kimlik bilgisinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="37dcc-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="37dcc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37dcc-117">PARAMETERS</span></span>

### <span data-ttu-id="37dcc-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37dcc-118">-AutomationAccountName</span></span>
<span data-ttu-id="37dcc-119">Bu cmdlet 'in kimlik bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37dcc-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="37dcc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dcc-120">-DefaultProfile</span></span>
<span data-ttu-id="37dcc-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="37dcc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37dcc-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="37dcc-122">-Name</span></span>
<span data-ttu-id="37dcc-123">Alınacak kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37dcc-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="37dcc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37dcc-124">-ResourceGroupName</span></span>
<span data-ttu-id="37dcc-125">Bu cmdlet 'in kimlik bilgilerini aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="37dcc-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="37dcc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dcc-126">CommonParameters</span></span>
<span data-ttu-id="37dcc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37dcc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dcc-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dcc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dcc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37dcc-129">INPUTS</span></span>

### <span data-ttu-id="37dcc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="37dcc-130">System.String</span></span>

## <span data-ttu-id="37dcc-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37dcc-131">OUTPUTS</span></span>

### <span data-ttu-id="37dcc-132">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="37dcc-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="37dcc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37dcc-133">NOTES</span></span>

## <span data-ttu-id="37dcc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37dcc-134">RELATED LINKS</span></span>

[<span data-ttu-id="37dcc-135">Yeni-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="37dcc-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="37dcc-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="37dcc-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="37dcc-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="37dcc-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


