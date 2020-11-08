---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4370FF88-E34F-499D-AF57-53C15B4EB6E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: e55d9e54dcaa0f547d64ec58b2772a581a8ec30a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106484"
---
# <span data-ttu-id="b2feb-101">Remove-AzureAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="b2feb-101">Remove-AzureAutomationConnectionType</span></span>

## <span data-ttu-id="b2feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2feb-102">SYNOPSIS</span></span>

<span data-ttu-id="b2feb-103">Bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b2feb-103">Removes a connection type.</span></span>

## <span data-ttu-id="b2feb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2feb-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnectionType -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2feb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2feb-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b2feb-106">**Remove-AzureAutomationConnectionType** cmdlet 'ı bir Azure Otomasyonu bağlantı türünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b2feb-106">The **Remove-AzureAutomationConnectionType** cmdlet removes an Azure Automation connection type.</span></span>

## <span data-ttu-id="b2feb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2feb-107">EXAMPLES</span></span>

## <span data-ttu-id="b2feb-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2feb-108">PARAMETERS</span></span>

### <span data-ttu-id="b2feb-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2feb-109">-AutomationAccountName</span></span>
<span data-ttu-id="b2feb-110">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2feb-110">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="b2feb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b2feb-111">-Force</span></span>
<span data-ttu-id="b2feb-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b2feb-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2feb-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2feb-113">-Name</span></span>
<span data-ttu-id="b2feb-114">Kaldırılacak bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2feb-114">Specifies the name of the connection type to remove.</span></span>

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

### <span data-ttu-id="b2feb-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2feb-115">-Profile</span></span>
<span data-ttu-id="b2feb-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2feb-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2feb-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b2feb-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2feb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2feb-118">CommonParameters</span></span>
<span data-ttu-id="b2feb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2feb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2feb-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2feb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2feb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2feb-121">INPUTS</span></span>

## <span data-ttu-id="b2feb-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2feb-122">OUTPUTS</span></span>

## <span data-ttu-id="b2feb-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2feb-123">NOTES</span></span>

## <span data-ttu-id="b2feb-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2feb-124">RELATED LINKS</span></span>

