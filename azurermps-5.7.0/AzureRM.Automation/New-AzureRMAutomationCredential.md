---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: 59a1b7bc849767f8d7d389631a69ae1fc93dc759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764191"
---
# <span data-ttu-id="bf355-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf355-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="bf355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf355-102">SYNOPSIS</span></span>
<span data-ttu-id="bf355-103">Otomasyon kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf355-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf355-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf355-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf355-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf355-105">DESCRIPTION</span></span>
<span data-ttu-id="bf355-106">**Yeni-AzureRmAutomationCredential** cmdlet 'ı, Azure Otomasyonu 'Nda bir **PSCredential** nesnesi olarak kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf355-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="bf355-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf355-107">EXAMPLES</span></span>

### <span data-ttu-id="bf355-108">Örnek 1: kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bf355-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bf355-109">İlk komut $User değişkenine bir Kullanıcı adı atar.</span><span class="sxs-lookup"><span data-stu-id="bf355-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="bf355-110">İkinci komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="bf355-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="bf355-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bf355-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="bf355-112">Üçüncü komut $User ve $Password dayalı bir kimlik bilgisi oluşturur ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bf355-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="bf355-113">Son komutu, $Credential kullanan Contosocontosocredential adlı bir Otomasyon kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf355-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="bf355-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf355-114">PARAMETERS</span></span>

### <span data-ttu-id="bf355-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf355-115">-AutomationAccountName</span></span>
<span data-ttu-id="bf355-116">Bu cmdlet 'in kimlik bilgilerini sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf355-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="bf355-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf355-117">-DefaultProfile</span></span>
<span data-ttu-id="bf355-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bf355-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf355-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="bf355-119">-Description</span></span>
<span data-ttu-id="bf355-120">Kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf355-120">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf355-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf355-121">-Name</span></span>
<span data-ttu-id="bf355-122">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf355-122">Specifies a name for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf355-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf355-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf355-124">Bu cmdlet 'in kimlik bilgileri oluşturduğu kaynak grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf355-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="bf355-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="bf355-125">-Value</span></span>
<span data-ttu-id="bf355-126">Kimlik bilgilerini **PSCredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf355-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf355-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf355-127">CommonParameters</span></span>
<span data-ttu-id="bf355-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf355-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf355-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf355-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf355-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf355-130">INPUTS</span></span>

### <span data-ttu-id="bf355-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bf355-131">None</span></span>
<span data-ttu-id="bf355-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="bf355-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf355-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf355-133">OUTPUTS</span></span>

### <span data-ttu-id="bf355-134">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="bf355-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="bf355-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf355-135">NOTES</span></span>

## <span data-ttu-id="bf355-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf355-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf355-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf355-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="bf355-138">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf355-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="bf355-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="bf355-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


