---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: 5f6ff2e89bd3b84a573e02a4584fe69794829453
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762178"
---
# <span data-ttu-id="33fd2-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33fd2-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="33fd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="33fd2-103">Otomasyon kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="33fd2-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33fd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33fd2-104">SYNTAX</span></span>

### <span data-ttu-id="33fd2-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33fd2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33fd2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="33fd2-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33fd2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="33fd2-107">DESCRIPTION</span></span>
<span data-ttu-id="33fd2-108">**Get-AzureRmAutomationCredential** cmdlet 'i bir veya daha çok Azure Otomasyonu kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="33fd2-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="33fd2-109">Varsayılan olarak, tüm kimlik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="33fd2-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="33fd2-110">Belirli bir kimlik bilgisinin alınacağı kimlik bilgisinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="33fd2-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="33fd2-111">Güvenlik amaçları doğrultusunda bu cmdlet kimlik bilgileri parolalarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="33fd2-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="33fd2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33fd2-112">EXAMPLES</span></span>

### <span data-ttu-id="33fd2-113">Örnek 1: tüm kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="33fd2-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="33fd2-114">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm kimlik bilgilerinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="33fd2-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="33fd2-115">Örnek 2: kimlik bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="33fd2-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="33fd2-116">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoCredential adlı kimlik bilgisinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="33fd2-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="33fd2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33fd2-117">PARAMETERS</span></span>

### <span data-ttu-id="33fd2-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33fd2-118">-AutomationAccountName</span></span>
<span data-ttu-id="33fd2-119">Bu cmdlet 'in kimlik bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33fd2-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="33fd2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fd2-120">-DefaultProfile</span></span>
<span data-ttu-id="33fd2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="33fd2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33fd2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="33fd2-122">-Name</span></span>
<span data-ttu-id="33fd2-123">Alınacak kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33fd2-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fd2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33fd2-124">-ResourceGroupName</span></span>
<span data-ttu-id="33fd2-125">Bu cmdlet 'in kimlik bilgilerini aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="33fd2-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="33fd2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fd2-126">CommonParameters</span></span>
<span data-ttu-id="33fd2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33fd2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fd2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33fd2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fd2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33fd2-129">INPUTS</span></span>

### <span data-ttu-id="33fd2-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33fd2-130">None</span></span>
<span data-ttu-id="33fd2-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="33fd2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33fd2-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33fd2-132">OUTPUTS</span></span>

### <span data-ttu-id="33fd2-133">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="33fd2-133">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="33fd2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33fd2-134">NOTES</span></span>

## <span data-ttu-id="33fd2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33fd2-135">RELATED LINKS</span></span>

[<span data-ttu-id="33fd2-136">Yeni-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33fd2-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="33fd2-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33fd2-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="33fd2-138">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="33fd2-138">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


