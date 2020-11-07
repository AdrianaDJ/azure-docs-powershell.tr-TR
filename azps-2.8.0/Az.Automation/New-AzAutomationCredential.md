---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a4d28affaa44e96a713adea7935073bcdf9d93c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753278"
---
# <span data-ttu-id="908dd-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="908dd-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="908dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="908dd-102">SYNOPSIS</span></span>
<span data-ttu-id="908dd-103">Otomasyon kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="908dd-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="908dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="908dd-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="908dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="908dd-105">DESCRIPTION</span></span>
<span data-ttu-id="908dd-106">**New-AzAutomationCredential** cmdlet 'ı Azure Otomasyonu 'Nda **PSCredential** nesnesi olarak bir kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="908dd-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="908dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="908dd-107">EXAMPLES</span></span>

### <span data-ttu-id="908dd-108">Örnek 1: kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="908dd-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="908dd-109">İlk komut $User değişkenine bir Kullanıcı adı atar.</span><span class="sxs-lookup"><span data-stu-id="908dd-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="908dd-110">İkinci komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dizeye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="908dd-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="908dd-111">Komut bu nesneyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="908dd-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="908dd-112">Üçüncü komut $User ve $Password dayalı bir kimlik bilgisi oluşturur ve $Credential değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="908dd-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="908dd-113">Son komutu, $Credential kullanan Contosocontosocredential adlı bir Otomasyon kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="908dd-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="908dd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="908dd-114">PARAMETERS</span></span>

### <span data-ttu-id="908dd-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="908dd-115">-AutomationAccountName</span></span>
<span data-ttu-id="908dd-116">Bu cmdlet 'in kimlik bilgilerini sakladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908dd-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="908dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908dd-117">-DefaultProfile</span></span>
<span data-ttu-id="908dd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="908dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="908dd-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="908dd-119">-Description</span></span>
<span data-ttu-id="908dd-120">Kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908dd-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="908dd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="908dd-121">-Name</span></span>
<span data-ttu-id="908dd-122">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908dd-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="908dd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908dd-123">-ResourceGroupName</span></span>
<span data-ttu-id="908dd-124">Bu cmdlet 'in kimlik bilgileri oluşturduğu kaynak grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="908dd-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="908dd-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="908dd-125">-Value</span></span>
<span data-ttu-id="908dd-126">Kimlik bilgilerini **PSCredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="908dd-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="908dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908dd-127">CommonParameters</span></span>
<span data-ttu-id="908dd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="908dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908dd-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908dd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908dd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="908dd-130">INPUTS</span></span>

### <span data-ttu-id="908dd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="908dd-131">System.String</span></span>

### <span data-ttu-id="908dd-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="908dd-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="908dd-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="908dd-133">OUTPUTS</span></span>

### <span data-ttu-id="908dd-134">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="908dd-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="908dd-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="908dd-135">NOTES</span></span>

## <span data-ttu-id="908dd-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="908dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="908dd-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="908dd-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="908dd-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="908dd-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="908dd-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="908dd-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)

