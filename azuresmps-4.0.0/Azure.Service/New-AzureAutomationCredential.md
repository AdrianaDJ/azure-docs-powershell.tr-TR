---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106221"
---
# <span data-ttu-id="eee23-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eee23-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="eee23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee23-102">SYNOPSIS</span></span>

<span data-ttu-id="eee23-103">Otomasyon 'da kimlik bilgileri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eee23-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="eee23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eee23-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eee23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eee23-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="eee23-106">**New-AzureAutomationCredential** cmdlet 'ı, Microsoft Azure Otomasyonu 'Nda bir **PSCredential** nesnesi olarak kimlik bilgilerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eee23-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="eee23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eee23-107">EXAMPLES</span></span>

### <span data-ttu-id="eee23-108">Örnek 1: kimlik bilgisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="eee23-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="eee23-109">Bu komutlar MyCredential adlı bir kimlik bilgisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eee23-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="eee23-110">İlk olarak Kullanıcı adı ve parola içeren bir kimlik bilgisi nesnesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eee23-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="eee23-111">Bu daha sonra son komutta Otomasyon kimlik bilgilerini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="eee23-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="eee23-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eee23-112">PARAMETERS</span></span>

### <span data-ttu-id="eee23-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eee23-113">-AutomationAccountName</span></span>
<span data-ttu-id="eee23-114">Kimlik bilgisinin saklanacağı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee23-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="eee23-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="eee23-115">-Description</span></span>
<span data-ttu-id="eee23-116">Kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee23-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="eee23-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="eee23-117">-Name</span></span>
<span data-ttu-id="eee23-118">Kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee23-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="eee23-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="eee23-119">-Profile</span></span>
<span data-ttu-id="eee23-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee23-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eee23-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="eee23-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eee23-122">-Değer</span><span class="sxs-lookup"><span data-stu-id="eee23-122">-Value</span></span>
<span data-ttu-id="eee23-123">Kimlik bilgilerini **PSCredential** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="eee23-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eee23-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee23-124">CommonParameters</span></span>
<span data-ttu-id="eee23-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eee23-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee23-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee23-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee23-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eee23-127">INPUTS</span></span>

## <span data-ttu-id="eee23-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eee23-128">OUTPUTS</span></span>

### <span data-ttu-id="eee23-129">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="eee23-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="eee23-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eee23-130">NOTES</span></span>

## <span data-ttu-id="eee23-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eee23-131">RELATED LINKS</span></span>

[<span data-ttu-id="eee23-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eee23-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="eee23-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eee23-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="eee23-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="eee23-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


