---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106495"
---
# <span data-ttu-id="1a605-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1a605-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="1a605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a605-102">SYNOPSIS</span></span>

<span data-ttu-id="1a605-103">Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a605-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="1a605-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a605-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a605-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a605-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1a605-106">**Remove-AzureAutomationAccount** cmdlet 'ı Microsoft Azure Otomasyonu 'ndan bir hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a605-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="1a605-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a605-107">EXAMPLES</span></span>

### <span data-ttu-id="1a605-108">Örnek 1: Otomasyon hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1a605-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="1a605-109">Bu komut, kullanıcı doğrulaması istemeden MyAutomationAccount adlı bir Otomasyon hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1a605-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="1a605-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a605-110">PARAMETERS</span></span>

### <span data-ttu-id="1a605-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1a605-111">-Force</span></span>
<span data-ttu-id="1a605-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1a605-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1a605-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a605-113">-Name</span></span>
<span data-ttu-id="1a605-114">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a605-114">Specifies the name of the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a605-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a605-115">-Profile</span></span>
<span data-ttu-id="1a605-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a605-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a605-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1a605-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a605-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a605-118">CommonParameters</span></span>
<span data-ttu-id="1a605-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a605-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a605-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a605-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a605-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a605-121">INPUTS</span></span>

## <span data-ttu-id="1a605-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a605-122">OUTPUTS</span></span>

## <span data-ttu-id="1a605-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a605-123">NOTES</span></span>

## <span data-ttu-id="1a605-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a605-124">RELATED LINKS</span></span>

[<span data-ttu-id="1a605-125">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1a605-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="1a605-126">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1a605-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


