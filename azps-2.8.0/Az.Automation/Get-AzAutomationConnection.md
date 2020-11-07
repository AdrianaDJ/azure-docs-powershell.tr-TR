---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 267c18ea4abf87936c47629eca523b254b411240
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753346"
---
# <span data-ttu-id="c8b21-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c8b21-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="c8b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8b21-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b21-103">Otomasyon bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="c8b21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8b21-104">SYNTAX</span></span>

### <span data-ttu-id="c8b21-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8b21-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8b21-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="c8b21-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8b21-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="c8b21-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8b21-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8b21-108">DESCRIPTION</span></span>
<span data-ttu-id="c8b21-109">**Get-AzAutomationConnection** cmdlet 'i, bir veya daha fazla Azure Automation bağlantısını alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="c8b21-110">Varsayılan olarak, bu cmdlet tüm bağlantıları alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="c8b21-111">Belirli bir bağlantı almak için bağlantının adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c8b21-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="c8b21-112">Belirli bir türdeki tüm bağlantıları almak için bağlantı türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c8b21-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="c8b21-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8b21-113">EXAMPLES</span></span>

### <span data-ttu-id="c8b21-114">Örnek 1: tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="c8b21-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c8b21-115">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm bağlantıların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c8b21-116">Örnek 2: bir türdeki tüm bağlantıları alma</span><span class="sxs-lookup"><span data-stu-id="c8b21-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="c8b21-117">Bu komut, Contoso17 adlı Otomasyon hesabındaki bağlantıların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c8b21-118">Bu komut, SqlServer türünün bağlantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="c8b21-119">Örnek 3: bağlantı alma</span><span class="sxs-lookup"><span data-stu-id="c8b21-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="c8b21-120">Bu komut, ContosoConnection adlı bağlantı için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="c8b21-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="c8b21-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8b21-121">PARAMETERS</span></span>

### <span data-ttu-id="c8b21-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c8b21-122">-AutomationAccountName</span></span>
<span data-ttu-id="c8b21-123">Bu cmdlet 'in bağlantıları aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8b21-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b21-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="c8b21-124">-ConnectionTypeName</span></span>
<span data-ttu-id="c8b21-125">Bu cmdlet 'in bağlantıları aldığı bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8b21-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b21-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b21-126">-DefaultProfile</span></span>
<span data-ttu-id="c8b21-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8b21-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8b21-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8b21-128">-Name</span></span>
<span data-ttu-id="c8b21-129">Bu cmdlet 'in aldığı bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8b21-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b21-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8b21-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8b21-131">Bu cmdlet 'in bağlantıları aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8b21-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b21-132">CommonParameters</span></span>
<span data-ttu-id="c8b21-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8b21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b21-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b21-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b21-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8b21-135">INPUTS</span></span>

### <span data-ttu-id="c8b21-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c8b21-136">System.String</span></span>

## <span data-ttu-id="c8b21-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8b21-137">OUTPUTS</span></span>

### <span data-ttu-id="c8b21-138">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="c8b21-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="c8b21-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8b21-139">NOTES</span></span>

## <span data-ttu-id="c8b21-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8b21-140">RELATED LINKS</span></span>

[<span data-ttu-id="c8b21-141">Yeni-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c8b21-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="c8b21-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c8b21-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


