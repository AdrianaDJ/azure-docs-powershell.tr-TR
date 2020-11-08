---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105831"
---
# <span data-ttu-id="d9a49-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d9a49-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="d9a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a49-102">SYNOPSIS</span></span>

<span data-ttu-id="d9a49-103">Otomasyon 'da kimlik bilgilerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="d9a49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9a49-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9a49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9a49-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d9a49-106">**Set-AzureAutomationCredential** cmdlet 'ı, Microsoft Azure Otomasyonu 'nda bir kimlik bilgisini **PSCredential** nesnesi olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="d9a49-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9a49-107">EXAMPLES</span></span>

### <span data-ttu-id="d9a49-108">Örnek 1: kimlik bilgilerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d9a49-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="d9a49-109">Bu komutlar MyCredential adlı varolan bir kimlik bilgisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="d9a49-110">İlk olarak Kullanıcı adı ve parola içeren bir kimlik bilgisi nesnesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d9a49-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="d9a49-111">Bu daha sonra son komutta Otomasyon kimlik bilgilerini güncelleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d9a49-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="d9a49-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9a49-112">PARAMETERS</span></span>

### <span data-ttu-id="d9a49-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9a49-113">-AutomationAccountName</span></span>
<span data-ttu-id="d9a49-114">Kimlik bilgisiyle Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-114">Specifies the name of the Automation account with the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a49-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d9a49-115">-Description</span></span>
<span data-ttu-id="d9a49-116">Kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="d9a49-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9a49-117">-Name</span></span>
<span data-ttu-id="d9a49-118">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-118">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a49-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9a49-119">-Profile</span></span>
<span data-ttu-id="d9a49-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9a49-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d9a49-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a49-122">-Değer</span><span class="sxs-lookup"><span data-stu-id="d9a49-122">-Value</span></span>
<span data-ttu-id="d9a49-123">Kimlik bilgilerini **PSCredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9a49-123">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="d9a49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a49-124">CommonParameters</span></span>
<span data-ttu-id="d9a49-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9a49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a49-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a49-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a49-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9a49-127">INPUTS</span></span>

## <span data-ttu-id="d9a49-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9a49-128">OUTPUTS</span></span>

### <span data-ttu-id="d9a49-129">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="d9a49-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="d9a49-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9a49-130">NOTES</span></span>

## <span data-ttu-id="d9a49-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9a49-131">RELATED LINKS</span></span>

[<span data-ttu-id="d9a49-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d9a49-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="d9a49-133">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d9a49-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="d9a49-134">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d9a49-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


