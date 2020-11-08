---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106480"
---
# <span data-ttu-id="ccc98-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ccc98-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="ccc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccc98-102">SYNOPSIS</span></span>

<span data-ttu-id="ccc98-103">Otomasyon 'dan kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ccc98-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="ccc98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccc98-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ccc98-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccc98-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ccc98-106">**Remove-AzureAutomationCredential** cmdlet 'ı Microsoft Azure Otomasyonu 'ndan kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ccc98-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="ccc98-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccc98-107">EXAMPLES</span></span>

### <span data-ttu-id="ccc98-108">Örnek 1: kimlik bilgisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ccc98-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="ccc98-109">Bu komut, Contoso17 adlı Otomasyon hesabında MyCredential adlı kimlik bilgisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ccc98-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ccc98-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccc98-110">PARAMETERS</span></span>

### <span data-ttu-id="ccc98-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ccc98-111">-AutomationAccountName</span></span>
<span data-ttu-id="ccc98-112">Kimlik bilgisiyle Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccc98-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="ccc98-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ccc98-113">-Force</span></span>
<span data-ttu-id="ccc98-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ccc98-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc98-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ccc98-115">-Name</span></span>
<span data-ttu-id="ccc98-116">Kaldırılacak kimlik bilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccc98-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="ccc98-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ccc98-117">-Profile</span></span>
<span data-ttu-id="ccc98-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccc98-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ccc98-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ccc98-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ccc98-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc98-120">CommonParameters</span></span>
<span data-ttu-id="ccc98-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccc98-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc98-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc98-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc98-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccc98-123">INPUTS</span></span>

## <span data-ttu-id="ccc98-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccc98-124">OUTPUTS</span></span>

## <span data-ttu-id="ccc98-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccc98-125">NOTES</span></span>

## <span data-ttu-id="ccc98-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccc98-126">RELATED LINKS</span></span>

[<span data-ttu-id="ccc98-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ccc98-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="ccc98-128">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ccc98-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="ccc98-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ccc98-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


