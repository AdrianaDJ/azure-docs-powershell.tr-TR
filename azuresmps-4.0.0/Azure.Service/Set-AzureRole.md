---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105824"
---
# <span data-ttu-id="988df-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="988df-101">Set-AzureRole</span></span>

## <span data-ttu-id="988df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="988df-102">SYNOPSIS</span></span>
<span data-ttu-id="988df-103">Bir Azure rolünün örnek sayısını çalıştırılacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="988df-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="988df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="988df-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="988df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="988df-105">DESCRIPTION</span></span>
<span data-ttu-id="988df-106">**Set-AzureRole** cmdlet 'i, belirli bir rolün Azure dağıtımında çalışacağı örneklerinin sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="988df-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="988df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="988df-107">EXAMPLES</span></span>

### <span data-ttu-id="988df-108">1: rol için örnek sayısını ayarlama</span><span class="sxs-lookup"><span data-stu-id="988df-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="988df-109">Bu komut, MySvc01 hizmetinde üretimde çalışan MyTestRole03 rolünü üç örnek olacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="988df-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="988df-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="988df-110">PARAMETERS</span></span>

### <span data-ttu-id="988df-111">-Sayı</span><span class="sxs-lookup"><span data-stu-id="988df-111">-Count</span></span>
<span data-ttu-id="988df-112">Çalıştırılacak rol örneklerinin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988df-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="988df-113">-InformationAction</span></span>
<span data-ttu-id="988df-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="988df-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="988df-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="988df-116">'A</span><span class="sxs-lookup"><span data-stu-id="988df-116">Continue</span></span>
- <span data-ttu-id="988df-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="988df-117">Ignore</span></span>
- <span data-ttu-id="988df-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="988df-118">Inquire</span></span>
- <span data-ttu-id="988df-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="988df-119">SilentlyContinue</span></span>
- <span data-ttu-id="988df-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="988df-120">Stop</span></span>
- <span data-ttu-id="988df-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="988df-121">Suspend</span></span>

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

### <span data-ttu-id="988df-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="988df-122">-InformationVariable</span></span>
<span data-ttu-id="988df-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="988df-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="988df-124">-Profile</span></span>
<span data-ttu-id="988df-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="988df-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="988df-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="988df-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="988df-127">-RoleName</span></span>
<span data-ttu-id="988df-128">Örnek sayısını ayarlanacak rolün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-128">Specifies the name of the role for which to set the number of instances.</span></span>

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

### <span data-ttu-id="988df-129">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="988df-129">-ServiceName</span></span>
<span data-ttu-id="988df-130">Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="988df-131">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="988df-131">-Slot</span></span>
<span data-ttu-id="988df-132">Değiştirilecek dağıtımın dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="988df-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="988df-133">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="988df-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="988df-134">Üretim</span><span class="sxs-lookup"><span data-stu-id="988df-134">Production</span></span>
- <span data-ttu-id="988df-135">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="988df-135">Staging</span></span>

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

### <span data-ttu-id="988df-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988df-136">CommonParameters</span></span>
<span data-ttu-id="988df-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="988df-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988df-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988df-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988df-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="988df-139">INPUTS</span></span>

## <span data-ttu-id="988df-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="988df-140">OUTPUTS</span></span>

## <span data-ttu-id="988df-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="988df-141">NOTES</span></span>

## <span data-ttu-id="988df-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="988df-142">RELATED LINKS</span></span>

[<span data-ttu-id="988df-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="988df-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


