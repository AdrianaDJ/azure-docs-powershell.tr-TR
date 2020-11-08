---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105659"
---
# <span data-ttu-id="1ba60-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ba60-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="1ba60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba60-102">SYNOPSIS</span></span>

<span data-ttu-id="1ba60-103">Bir Azure Otomasyonu kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1ba60-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="1ba60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ba60-104">SYNTAX</span></span>

### <span data-ttu-id="1ba60-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ba60-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1ba60-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1ba60-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ba60-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ba60-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1ba60-108">**Get-AzureAutomationCredential** cmdlet 'i bir veya daha fazla Microsoft Azure Otomasyonu kimlik bilgisini alır.</span><span class="sxs-lookup"><span data-stu-id="1ba60-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="1ba60-109">Varsayılan olarak, tüm kimlik bilgileri verilir.</span><span class="sxs-lookup"><span data-stu-id="1ba60-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="1ba60-110">Belirli bir kimlik bilgilerini almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1ba60-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="1ba60-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ba60-111">EXAMPLES</span></span>

### <span data-ttu-id="1ba60-112">Örnek 1: tüm kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="1ba60-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1ba60-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="1ba60-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1ba60-114">Örnek 2: kimlik bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="1ba60-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="1ba60-115">Bu komut MyCredential adlı kimlik bilgisini alır.</span><span class="sxs-lookup"><span data-stu-id="1ba60-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="1ba60-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ba60-116">PARAMETERS</span></span>

### <span data-ttu-id="1ba60-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ba60-117">-AutomationAccountName</span></span>
<span data-ttu-id="1ba60-118">Alınacak kimlik bilgilerini içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba60-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

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

### <span data-ttu-id="1ba60-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ba60-119">-Name</span></span>
<span data-ttu-id="1ba60-120">Alınacak kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba60-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba60-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="1ba60-121">-Profile</span></span>
<span data-ttu-id="1ba60-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba60-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ba60-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1ba60-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ba60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba60-124">CommonParameters</span></span>
<span data-ttu-id="1ba60-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ba60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba60-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba60-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba60-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ba60-127">INPUTS</span></span>

## <span data-ttu-id="1ba60-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ba60-128">OUTPUTS</span></span>

### <span data-ttu-id="1ba60-129">Microsoft. Azure. Commands. Automation. model. Credentialınfo</span><span class="sxs-lookup"><span data-stu-id="1ba60-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="1ba60-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ba60-130">NOTES</span></span>

## <span data-ttu-id="1ba60-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ba60-131">RELATED LINKS</span></span>

[<span data-ttu-id="1ba60-132">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ba60-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="1ba60-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ba60-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="1ba60-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ba60-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


