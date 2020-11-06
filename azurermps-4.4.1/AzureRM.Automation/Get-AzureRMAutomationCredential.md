---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: f00cbe95c71bdbd8c7f92f123756fa0c474d878f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595043"
---
# <span data-ttu-id="3ae9d-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ae9d-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="3ae9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae9d-103">Otomasyon kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ae9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ae9d-104">SYNTAX</span></span>

### <span data-ttu-id="3ae9d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ae9d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ae9d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3ae9d-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ae9d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ae9d-108">**Get-AzureRmAutomationCredential** cmdlet 'i bir veya daha çok Azure Otomasyonu kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="3ae9d-109">Varsayılan olarak, tüm kimlik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="3ae9d-110">Belirli bir kimlik bilgisinin alınacağı kimlik bilgisinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="3ae9d-111">Güvenlik amaçları doğrultusunda bu cmdlet kimlik bilgileri parolalarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="3ae9d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ae9d-112">EXAMPLES</span></span>

### <span data-ttu-id="3ae9d-113">Örnek 1: tüm kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="3ae9d-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3ae9d-114">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm kimlik bilgilerinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ae9d-115">Örnek 2: kimlik bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="3ae9d-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="3ae9d-116">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoCredential adlı kimlik bilgisinin meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3ae9d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ae9d-117">PARAMETERS</span></span>

### <span data-ttu-id="3ae9d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ae9d-118">-AutomationAccountName</span></span>
<span data-ttu-id="3ae9d-119">Bu cmdlet 'in kimlik bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="3ae9d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ae9d-120">-Name</span></span>
<span data-ttu-id="3ae9d-121">Alınacak kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-121">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="3ae9d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae9d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ae9d-123">Bu cmdlet 'in kimlik bilgilerini aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-123">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="3ae9d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae9d-124">-DefaultProfile</span></span>
<span data-ttu-id="3ae9d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ae9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae9d-126">CommonParameters</span></span>
<span data-ttu-id="3ae9d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ae9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae9d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae9d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae9d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ae9d-129">INPUTS</span></span>

## <span data-ttu-id="3ae9d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ae9d-130">OUTPUTS</span></span>

### <span data-ttu-id="3ae9d-131">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="3ae9d-131">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="3ae9d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ae9d-132">NOTES</span></span>

## <span data-ttu-id="3ae9d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ae9d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ae9d-134">Yeni-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ae9d-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="3ae9d-135">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ae9d-135">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="3ae9d-136">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ae9d-136">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


