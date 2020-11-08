---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106370"
---
# <span data-ttu-id="749a0-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="749a0-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="749a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="749a0-102">SYNOPSIS</span></span>

<span data-ttu-id="749a0-103">Bir Azure Otomasyonu bağlantısı alır.</span><span class="sxs-lookup"><span data-stu-id="749a0-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="749a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="749a0-104">SYNTAX</span></span>

### <span data-ttu-id="749a0-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="749a0-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="749a0-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="749a0-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="749a0-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="749a0-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="749a0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="749a0-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="749a0-109">**Get-AzureAutomationConnection** cmdlet 'i bir veya daha fazla Microsoft Azure Automation bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="749a0-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="749a0-110">Varsayılan olarak, tüm bağlantılar verilir.</span><span class="sxs-lookup"><span data-stu-id="749a0-110">By default, all connections are returned.</span></span>
<span data-ttu-id="749a0-111">Belirli bir bağlantı almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="749a0-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="749a0-112">Belirli bir türdeki tüm bağlantıları almak için, bağlantı türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="749a0-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="749a0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="749a0-113">EXAMPLES</span></span>

### <span data-ttu-id="749a0-114">Örnek 1: tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="749a0-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="749a0-115">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm bağlantıları alır.</span><span class="sxs-lookup"><span data-stu-id="749a0-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="749a0-116">Örnek 2: bir türdeki tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="749a0-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="749a0-117">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm Azure bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="749a0-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="749a0-118">Örnek 3: bağlantı alma</span><span class="sxs-lookup"><span data-stu-id="749a0-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="749a0-119">Bu komut MyConnection adındaki bağlantıyı alır.</span><span class="sxs-lookup"><span data-stu-id="749a0-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="749a0-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="749a0-120">PARAMETERS</span></span>

### <span data-ttu-id="749a0-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="749a0-121">-AutomationAccountName</span></span>
<span data-ttu-id="749a0-122">Alınacak bağlantıyı içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="749a0-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="749a0-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="749a0-123">-ConnectionTypeName</span></span>
<span data-ttu-id="749a0-124">Bağlantıların alınacağı bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="749a0-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="749a0-125">-Name</span></span>
<span data-ttu-id="749a0-126">Alınacak bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="749a0-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="749a0-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="749a0-127">-Profile</span></span>
<span data-ttu-id="749a0-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="749a0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="749a0-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="749a0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="749a0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="749a0-130">CommonParameters</span></span>
<span data-ttu-id="749a0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="749a0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="749a0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="749a0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="749a0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="749a0-133">INPUTS</span></span>

## <span data-ttu-id="749a0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="749a0-134">OUTPUTS</span></span>

### <span data-ttu-id="749a0-135">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="749a0-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="749a0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="749a0-136">NOTES</span></span>

## <span data-ttu-id="749a0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="749a0-137">RELATED LINKS</span></span>

[<span data-ttu-id="749a0-138">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="749a0-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="749a0-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="749a0-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="749a0-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="749a0-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


