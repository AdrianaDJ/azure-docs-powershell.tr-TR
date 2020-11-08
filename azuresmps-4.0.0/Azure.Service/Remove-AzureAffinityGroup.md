---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106172"
---
# <span data-ttu-id="1e673-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e673-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="1e673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e673-102">SYNOPSIS</span></span>
<span data-ttu-id="1e673-103">Bir abonelikteki benzeşim grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="1e673-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="1e673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e673-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1e673-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e673-105">DESCRIPTION</span></span>
<span data-ttu-id="1e673-106">**Remove-AzureAffinityGroup** cmdlet 'i geçerli abonelikteki bir Azure benzeşim grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="1e673-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="1e673-107">Üyesi olan bir benzeşim grubunu silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e673-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="1e673-108">Önce bir benzeşim grubunun tüm üyelerini silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1e673-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="1e673-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e673-109">EXAMPLES</span></span>

### <span data-ttu-id="1e673-110">Örnek 1: benzeşim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="1e673-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="1e673-111">Bu komut geçerli abonelikteki South01 benzeşim grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="1e673-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="1e673-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e673-112">PARAMETERS</span></span>

### <span data-ttu-id="1e673-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1e673-113">-InformationAction</span></span>
<span data-ttu-id="1e673-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e673-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1e673-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1e673-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e673-116">'A</span><span class="sxs-lookup"><span data-stu-id="1e673-116">Continue</span></span>
- <span data-ttu-id="1e673-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="1e673-117">Ignore</span></span>
- <span data-ttu-id="1e673-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1e673-118">Inquire</span></span>
- <span data-ttu-id="1e673-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1e673-119">SilentlyContinue</span></span>
- <span data-ttu-id="1e673-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1e673-120">Stop</span></span>
- <span data-ttu-id="1e673-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1e673-121">Suspend</span></span>

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

### <span data-ttu-id="1e673-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1e673-122">-InformationVariable</span></span>
<span data-ttu-id="1e673-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e673-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1e673-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e673-124">-Name</span></span>
<span data-ttu-id="1e673-125">Bu cmdlet 'in sildiği benzeşim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e673-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1e673-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e673-126">-Profile</span></span>
<span data-ttu-id="1e673-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e673-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e673-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1e673-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e673-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e673-129">CommonParameters</span></span>
<span data-ttu-id="1e673-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e673-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e673-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e673-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e673-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e673-132">INPUTS</span></span>

## <span data-ttu-id="1e673-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e673-133">OUTPUTS</span></span>

## <span data-ttu-id="1e673-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e673-134">NOTES</span></span>

## <span data-ttu-id="1e673-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e673-135">RELATED LINKS</span></span>

[<span data-ttu-id="1e673-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e673-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="1e673-137">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e673-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="1e673-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="1e673-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


