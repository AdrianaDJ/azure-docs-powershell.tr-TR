---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591181"
---
# <span data-ttu-id="e5318-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5318-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="e5318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5318-102">SYNOPSIS</span></span>
<span data-ttu-id="e5318-103">Otomasyon kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5318-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5318-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5318-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5318-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5318-105">DESCRIPTION</span></span>
<span data-ttu-id="e5318-106">**Yeni-AzureRmAutomationCredential** cmdlet 'ı, Azure Otomasyonu 'Nda bir **PSCredential** nesnesi olarak kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5318-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="e5318-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5318-107">EXAMPLES</span></span>

### <span data-ttu-id="e5318-108">Örnek 1: kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5318-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5318-109">İlk komut $User değişkenine bir Kullanıcı adı atar.</span><span class="sxs-lookup"><span data-stu-id="e5318-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="e5318-110">İkinci komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="e5318-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e5318-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e5318-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="e5318-112">Üçüncü komut $User ve $Password dayalı bir kimlik bilgisi oluşturur ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e5318-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="e5318-113">Son komutu, $Credential kullanan Contosocontosocredential adlı bir Otomasyon kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5318-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="e5318-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5318-114">PARAMETERS</span></span>

### <span data-ttu-id="e5318-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5318-115">-AutomationAccountName</span></span>
<span data-ttu-id="e5318-116">Bu cmdlet 'in kimlik bilgilerini sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5318-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="e5318-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e5318-117">-Description</span></span>
<span data-ttu-id="e5318-118">Kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5318-118">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5318-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5318-119">-Name</span></span>
<span data-ttu-id="e5318-120">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5318-120">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="e5318-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5318-121">-ResourceGroupName</span></span>
<span data-ttu-id="e5318-122">Bu cmdlet 'in kimlik bilgileri oluşturduğu kaynak grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5318-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="e5318-123">-Değer</span><span class="sxs-lookup"><span data-stu-id="e5318-123">-Value</span></span>
<span data-ttu-id="e5318-124">Kimlik bilgilerini **PSCredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5318-124">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5318-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5318-125">-DefaultProfile</span></span>
<span data-ttu-id="e5318-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5318-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5318-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5318-127">CommonParameters</span></span>
<span data-ttu-id="e5318-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5318-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5318-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5318-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5318-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5318-130">INPUTS</span></span>

## <span data-ttu-id="e5318-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5318-131">OUTPUTS</span></span>

### <span data-ttu-id="e5318-132">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="e5318-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e5318-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5318-133">NOTES</span></span>

## <span data-ttu-id="e5318-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5318-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5318-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5318-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="e5318-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5318-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="e5318-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5318-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)

