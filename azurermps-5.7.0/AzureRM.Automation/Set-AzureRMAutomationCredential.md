---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: 30f88139bcd96f08dcb1c1263f5b5b5d1e35d4d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592976"
---
# <span data-ttu-id="448bc-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448bc-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="448bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448bc-102">SYNOPSIS</span></span>
<span data-ttu-id="448bc-103">Otomasyon kimlik bilgilerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="448bc-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="448bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="448bc-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="448bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="448bc-105">DESCRIPTION</span></span>
<span data-ttu-id="448bc-106">**Set-AzureRmAutomationCredential** cmdlet 'ı Azure Otomasyonu 'nda bir kimlik bilgisini **PSCredential** nesnesi olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="448bc-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="448bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="448bc-107">EXAMPLES</span></span>

### <span data-ttu-id="448bc-108">Örnek 1: kimlik bilgilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="448bc-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="448bc-109">İlk komut $User değişkenine bir Kullanıcı adı atar.</span><span class="sxs-lookup"><span data-stu-id="448bc-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="448bc-110">İkinci komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="448bc-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="448bc-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="448bc-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="448bc-112">Üçüncü komut $User ve $Password dayalı bir kimlik bilgisi oluşturur ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="448bc-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="448bc-113">Son komutu $Credential 'da kimlik bilgisini kullanmak için ContosoCredential adlı Otomasyon kimlik bilgilerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="448bc-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="448bc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="448bc-114">PARAMETERS</span></span>

### <span data-ttu-id="448bc-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="448bc-115">-AutomationAccountName</span></span>
<span data-ttu-id="448bc-116">Bu cmdlet 'in kimlik bilgilerini değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="448bc-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="448bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448bc-117">-DefaultProfile</span></span>
<span data-ttu-id="448bc-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="448bc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="448bc-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="448bc-119">-Description</span></span>
<span data-ttu-id="448bc-120">Bu cmdlet 'in değiştirdiği kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="448bc-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="448bc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="448bc-121">-Name</span></span>
<span data-ttu-id="448bc-122">Bu cmdlet 'in değiştirdiği kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="448bc-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="448bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="448bc-124">Bu cmdlet 'in kimlik bilgilerini değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="448bc-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="448bc-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="448bc-125">-Value</span></span>
<span data-ttu-id="448bc-126">Kimlik bilgilerini **PSCredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="448bc-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448bc-127">CommonParameters</span></span>
<span data-ttu-id="448bc-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="448bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448bc-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448bc-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="448bc-130">INPUTS</span></span>

### <span data-ttu-id="448bc-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="448bc-131">None</span></span>
<span data-ttu-id="448bc-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="448bc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="448bc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="448bc-133">OUTPUTS</span></span>

### <span data-ttu-id="448bc-134">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="448bc-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="448bc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="448bc-135">NOTES</span></span>

## <span data-ttu-id="448bc-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="448bc-136">RELATED LINKS</span></span>

[<span data-ttu-id="448bc-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448bc-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="448bc-138">Yeni-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448bc-138">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="448bc-139">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="448bc-139">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


