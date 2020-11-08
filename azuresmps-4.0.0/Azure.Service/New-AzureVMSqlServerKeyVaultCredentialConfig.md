---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106188"
---
# <span data-ttu-id="2ac2e-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="2ac2e-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="2ac2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac2e-102">SYNOPSIS</span></span>

## <span data-ttu-id="2ac2e-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ac2e-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ac2e-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ac2e-104">DESCRIPTION</span></span>

## <span data-ttu-id="2ac2e-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ac2e-105">EXAMPLES</span></span>

### <span data-ttu-id="2ac2e-106">2</span><span class="sxs-lookup"><span data-stu-id="2ac2e-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="2ac2e-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ac2e-107">PARAMETERS</span></span>

### <span data-ttu-id="2ac2e-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2ac2e-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2ac2e-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="2ac2e-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2ac2e-111">-InformationAction</span></span>
<span data-ttu-id="2ac2e-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac2e-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ac2e-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="2ac2e-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ac2e-114">'A</span><span class="sxs-lookup"><span data-stu-id="2ac2e-114">Continue</span></span>
- <span data-ttu-id="2ac2e-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="2ac2e-115">Ignore</span></span>
- <span data-ttu-id="2ac2e-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="2ac2e-116">Inquire</span></span>
- <span data-ttu-id="2ac2e-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="2ac2e-117">SilentlyContinue</span></span>
- <span data-ttu-id="2ac2e-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="2ac2e-118">Stop</span></span>
- <span data-ttu-id="2ac2e-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="2ac2e-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="2ac2e-120">-InformationVariable</span></span>
<span data-ttu-id="2ac2e-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac2e-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="2ac2e-122">-Profile</span></span>
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

### <span data-ttu-id="2ac2e-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2ac2e-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="2ac2e-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac2e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac2e-125">CommonParameters</span></span>
<span data-ttu-id="2ac2e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ac2e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac2e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac2e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac2e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ac2e-128">INPUTS</span></span>

## <span data-ttu-id="2ac2e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ac2e-129">OUTPUTS</span></span>

## <span data-ttu-id="2ac2e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ac2e-130">NOTES</span></span>

## <span data-ttu-id="2ac2e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ac2e-131">RELATED LINKS</span></span>

