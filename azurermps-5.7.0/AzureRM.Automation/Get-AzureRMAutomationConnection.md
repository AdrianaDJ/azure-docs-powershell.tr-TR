---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 85d2e5d3044efe97eef2b4aa784d8767973682f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587715"
---
# <span data-ttu-id="99f70-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="99f70-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="99f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f70-102">SYNOPSIS</span></span>
<span data-ttu-id="99f70-103">Otomasyon bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99f70-104">SYNTAX</span></span>

### <span data-ttu-id="99f70-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99f70-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f70-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="99f70-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f70-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="99f70-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f70-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="99f70-108">DESCRIPTION</span></span>
<span data-ttu-id="99f70-109">**Get-AzureRmAutomationConnection** cmdlet 'i bir veya daha fazla Azure Otomasyonu bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="99f70-110">Varsayılan olarak, bu cmdlet tüm bağlantıları alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="99f70-111">Belirli bir bağlantı almak için bağlantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="99f70-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="99f70-112">Belirli bir türdeki tüm bağlantıları almak için bağlantı türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="99f70-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="99f70-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99f70-113">EXAMPLES</span></span>

### <span data-ttu-id="99f70-114">Örnek 1: tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="99f70-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="99f70-115">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm bağlantıların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="99f70-116">Örnek 2: bir türdeki tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="99f70-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="99f70-117">Bu komut, Contoso17 adlı Otomasyon hesabındaki bağlantıların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="99f70-118">Bu komut, SqlServer türünün bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="99f70-119">Örnek 3: bağlantı alma</span><span class="sxs-lookup"><span data-stu-id="99f70-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="99f70-120">Bu komut, ContosoConnection adlı bağlantı için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="99f70-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="99f70-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99f70-121">PARAMETERS</span></span>

### <span data-ttu-id="99f70-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="99f70-122">-AutomationAccountName</span></span>
<span data-ttu-id="99f70-123">Bu cmdlet 'in bağlantıları aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99f70-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="99f70-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="99f70-124">-ConnectionTypeName</span></span>
<span data-ttu-id="99f70-125">Bu cmdlet 'in bağlantıları aldığı bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99f70-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f70-126">-DefaultProfile</span></span>
<span data-ttu-id="99f70-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="99f70-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f70-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="99f70-128">-Name</span></span>
<span data-ttu-id="99f70-129">Bu cmdlet 'in aldığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99f70-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f70-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f70-130">-ResourceGroupName</span></span>
<span data-ttu-id="99f70-131">Bu cmdlet 'in bağlantıları aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99f70-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="99f70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f70-132">CommonParameters</span></span>
<span data-ttu-id="99f70-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99f70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f70-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f70-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f70-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99f70-135">INPUTS</span></span>

### <span data-ttu-id="99f70-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="99f70-136">None</span></span>
<span data-ttu-id="99f70-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="99f70-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99f70-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99f70-138">OUTPUTS</span></span>

### <span data-ttu-id="99f70-139">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="99f70-139">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="99f70-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99f70-140">NOTES</span></span>

## <span data-ttu-id="99f70-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99f70-141">RELATED LINKS</span></span>

[<span data-ttu-id="99f70-142">Yeni-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="99f70-142">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="99f70-143">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="99f70-143">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


